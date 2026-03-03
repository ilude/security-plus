# Agents

Agent workflows for maintaining and expanding this study system.

## Gap Analysis

Identifies topics in the study materials that don't match the official CompTIA SY0-701 exam objectives.

**When to use:** After a student completes the exam and reports topics that weren't covered, or periodically to audit coverage.

**Workflow:**
1. Launch one agent per domain (or combine lighter domains like D1+D3)
2. Each agent reads `glossary.md`, `concept-walkthrough.md`, and `notes.md`
3. Agent researches official exam objectives from multiple authoritative sources
4. Agent rates each sub-objective as COVERED / PARTIAL / MISSING
5. Output: `tasks/gap-analysis-d{N}.md`

**Agent config:**
- Type: `general-purpose` (needs web search + file read)
- Run in background: yes (parallel across domains)
- Typical duration: 3-6 minutes per domain

## Content Builder

Writes new glossary sections to fill identified gaps.

**When to use:** After gap analysis identifies MISSING or PARTIAL objectives.

**Workflow:**
1. Launch one builder per domain
2. Each builder reads the gap analysis AND existing `glossary.md` for formatting
3. Builder writes new sections matching existing style (tables, decision rules, blockquotes)
4. Output: `tasks/new-glossary-d{N}.md` (separate files to avoid conflicts)
5. A final merge agent combines all new content into `glossary.md`

**Agent config:**
- Type: `builder` (needs file read + write)
- Run in background: yes (parallel across domains)
- Typical duration: 2-4 minutes per domain

**Formatting rules the builder must follow:**
- Table format: `| Acronym/Term | Full Name | What It Does |`
- Decision rules in `> **Decision Rules:**` blockquote sections
- Bold terms in tables
- 1-2 sentence descriptions per table entry
- Number sections sequentially from the last existing section

## Content Validator

Cross-references new content against official exam objectives to catch inaccuracies and omissions.

**When to use:** After content builders finish, before merging into `glossary.md`.

**Workflow:**
1. Launch one validator per domain (parallel with builders — validators research objectives while builders write)
2. Each validator independently pulls official SY0-701 objectives from multiple sources
3. Validator reads the builder's output file and cross-references every item
4. Flags each item as: VALID / INFERRED / QUESTIONABLE / MISSING FROM CONTENT
5. Output: `tasks/validation-d{N}.md`

**Agent config:**
- Type: `general-purpose` (needs web search + file read)
- Run in background: yes
- Typical duration: 6-9 minutes per domain (longer than builders due to web research)

**Validation criteria:**
- VALID: Topic is explicitly listed in official CompTIA objectives
- INFERRED: Not explicitly listed but clearly implied by an objective
- QUESTIONABLE: May not be on the exam — too detailed or out of scope
- MISSING FROM CONTENT: In official objectives but not covered in new content

## Merge Agent

Combines validated content from multiple builder outputs into `glossary.md`.

**When to use:** After all builders and validators complete.

**Workflow:**
1. Read existing `glossary.md` and all `tasks/new-glossary-d{N}.md` files
2. Apply corrections identified by validators (add missing items, trim questionable ones)
3. Append new sections to `glossary.md`, preserving all existing content
4. Strip builder file headers, keep only section content

**Agent config:**
- Type: `builder` (needs file read + write)
- Run sequentially (single agent, touches the shared glossary file)
- Typical duration: 5-12 minutes

## Full Pipeline

Run all agents in sequence for a complete content refresh:

```
1. Gap Analysis    (4 agents, parallel, ~5 min)
2. Content Builder (4 agents, parallel, ~3 min)  }  can overlap —
3. Content Validator (4 agents, parallel, ~8 min) }  validators start researching while builders write
4. Merge           (1 agent, sequential, ~10 min)
5. Commit + push
```

Total wall-clock time: ~25-30 minutes for a full audit and backfill across all 5 domains.

## Known Issues

- Validators flag items as "MISSING FROM CONTENT" when they exist in the original glossary but not in the new supplement. This is expected — cross-reference against the full `glossary.md` before treating these as real gaps.
- Builder agents occasionally include topics from adjacent domains (e.g., Bluetooth attacks in a D4 section when they belong in D2). The merge agent should catch and relocate these based on validator feedback.
