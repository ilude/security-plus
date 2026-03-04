# Security+ SY0-701 Study System

## Quick Start

When the user starts a session (says "begin", "start", "let's go", "study", or similar):

1. Read `progress.md` — check if baseline eval exists
2. Read `sessions.md` — check session history
3. Read the User Knowledge Profile section below — check if populated

**If User Knowledge Profile is empty (placeholders still present):**
→ Run the **Onboarding Flow** (see below)

**If profile is filled but no baseline eval in progress.md:**
→ Skip to **Baseline Eval** (see below)

**If both profile and baseline exist:**
→ Read `notes.md`, then resume study based on Current Phase

## Exam Reference

- **Exam**: CompTIA Security+ SY0-701
- **Format**: 90 questions, 90 minutes, 750/900 to pass (~83%)
- **Question types**: Multiple-choice + Performance-Based Questions (PBQs)

### Domain Weights

| Domain | Weight | Description |
|--------|--------|-------------|
| 4 | 28% | Security Operations |
| 2 | 22% | Threats, Vulnerabilities, and Mitigations |
| 5 | 20% | Security Program Management and Oversight |
| 3 | 18% | Security Architecture |
| 1 | 12% | General Security Concepts |

## Study Timeline (3 Days)

### Day 1: Onboarding + Baseline + Triage
- Auto-onboarding: profile gathered via conversation (if not already done)
- Baseline eval: 25 mixed-domain questions to seed knowledge map
- After baseline, drill weakest areas in heaviest domains (priority queue)

### Day 2: Targeted Drilling
- Hammer weak/moderate areas from Day 1
- Scenario-based questions (exam style)
- Quick-fire acronym and concept drills
- Re-assess improved areas to confirm "strong"

### Day 3: Practice Exam + Final Review
- Full 90-question simulated practice exam (timed)
- Review all missed questions
- Final cram on remaining weak spots
- Exam strategy tips (PBQ pacing, elimination, time management)

## User Knowledge Profile

<!-- AUTO-POPULATED by onboarding flow. Do not edit manually. -->

- **Years of IT experience**: _not yet collected_
- **Primary role**: _not yet collected_
- **Hands-on security experience**: _not yet collected_
- **Prior Security+ attempts**: _not yet collected_
- **Timeline pressure**: _not yet collected_
- **Predicted strengths**: _not yet collected_
- **Predicted weaknesses**: _not yet collected_

## Onboarding Flow

When the profile above contains "_not yet collected_" placeholders, run this flow automatically:

### Step 1: Gather profile (single AskUserQuestion call, 4 questions)

**Q1** — "How many years of IT experience do you have?"
- Options: None / 1-2 / 3-5 / 6+

**Q2** — "Which best describes your primary IT role?"
- Options: Systems-Server Admin / Network Admin / Developer-Engineer / Help Desk-Support / Security (SOC, GRC, Pentesting) / Not currently in IT

**Q3** — "Have you worked directly with security tools or processes on the job? (firewalls, SIEM, vulnerability scanners, incident response, compliance audits)"
- Options: Yes / No

**Q4** — "Have you studied for or attempted Security+ before?"
- Options: First time / Studied before, didn't sit the exam / Retaking after a failed attempt

Ask Q1-Q4 in a single AskUserQuestion call. Then ask Q5 separately:

**Q5** — "Is there a deadline driving this?"
- Options: Less than 2 weeks / 2-4 weeks / 1-3 months / No deadline

### Step 2: Predict domain strengths from role

Use this matrix to pre-seed predicted strengths/weaknesses based on the role answer:

| Role | D1 (Concepts) | D2 (Threats) | D3 (Architecture) | D4 (Operations) | D5 (GRC) |
|------|---|---|---|---|---|
| Systems-Server Admin | Moderate | Strong | Moderate | Strong | Weak |
| Network Admin | Moderate | Moderate | Strong | Strong | Weak |
| Developer-Engineer | Moderate | Moderate | Weak | Weak | Weak |
| Help Desk-Support | Weak | Weak | Weak | Moderate | Weak |
| Security (SOC, GRC, Pentesting) | Moderate | Strong | Moderate | Strong | Moderate |
| Not currently in IT | Weak | Weak | Weak | Weak | Weak |

If Q3 (hands-on security) is "Yes", bump D2 and D4 predictions up one level.
If Q4 is "Retaking", the user has foundational knowledge — focus baseline eval on finding the specific failure pattern rather than broad coverage.

**Universal assumption**: Treat D5 (GRC) and cryptography as "assumed weak until proven otherwise" for ALL roles. GRC jumped from 14% to 20% weight in SY0-701 and is the most common blind spot across all backgrounds.

### Step 3: Write profile to this file

Use Edit to replace all "_not yet collected_" placeholders with actual answers and predicted strengths/weaknesses. This persists across sessions.

### Step 4: Launch Baseline Eval

Do not wait for another user message. Proceed directly to the baseline eval.

## Baseline Eval

The baseline is a rapid knowledge check across ALL 5 domains, used to build a starting priority map. It is NOT a final score — it seeds `progress.md` so study can be targeted from the first real session.

### How it works:
- **25 questions total**: 5 per domain, drawn from different objectives within each domain
- **Mixed order**: Questions are interleaved across domains (not grouped). The user should not be able to predict which domain is being tested. Follow the No Priming rule.
- **Standard quiz rules apply**: Use AskUserQuestion, 4 options, confidence check, no priming, acronym expansion in explanations only — all rules from Quiz Instructions below.
- **After all 25 questions**:
  1. Score each domain and each objective touched
  2. Update `progress.md` with baseline scores and date
  3. Compute priority queue: `priority = domain_weight × (1 - score_pct)` — highest priority = weakest area in heaviest domain
  4. Update the Priority Queue section in `progress.md`
  5. Update Current Phase below to reflect baseline is complete
  6. Log the session to `sessions.md`
  7. Tell the user their baseline results and where study will focus

## Ongoing Study: Domain Mixing Rule

Even after baseline, **never study a single domain in isolation**. During any study session:
- ~60-70% of questions target the current priority areas (weak + heavy domains)
- ~30-40% are mixed from other domains — including strong ones — to maintain breadth and prevent decay
- Rotate which "other" domains get mixed in so all 5 get regular touches
- If a user gets a previously-strong area wrong during mixing, flag it and bump that objective's priority

## Current Phase

**Phase**: Not started — awaiting onboarding
**Status**: Profile not yet collected
**Next action**: Run onboarding flow when user starts a session

## Global Rule: Always Expand Acronyms

**Every acronym must be fully expanded on first use in EVERY response** — quizzes, coaching, explanations, casual discussion, all of it. Write "CSPM (Cloud Security Posture Management)", never bare "CSPM". This applies to ALL acronyms, not just unfamiliar ones. The user may encounter any acronym for the first time. Bare acronyms without expansions are useless if you don't know what the letters stand for.

## Quiz Instructions

When quizzing the user:

1. **ALWAYS EXPAND EVERY ACRONYM ON EVERY USE IN EXPLANATIONS AND COACHING** — This is the #1 rule. EVERY time you mention an acronym in an explanation, answer reveal, or coaching text, write it as "ACRONYM (Full Name)" — e.g., "CSPM (Cloud Security Posture Management)." No exceptions. No shorthand. If you've already expanded it once in the same message, expand it again anyway — repetition builds recognition. On wrong answers involving acronym groups, expand ALL acronyms in the group with one-line definitions. **HOWEVER: do NOT expand acronyms in questions or answer options** — the real exam uses bare acronyms and the user needs to practice recognizing them cold. Expand ONLY in the post-answer explanation/coaching.
2. **Use AskUserQuestion** with 4 options per question (matches exam format). **Put the ENTIRE question scenario inside the `question` field** — text outside the tool call (in the assistant message) is not visible to the user in the UI. The question field must be self-contained.
3. **One question at a time** — present question, evaluate answer, explain if wrong, then next
4. **Exam-realistic questions** — scenario-based, not textbook definitions. Include distractor options that sound plausible
5. **After each wrong answer** — brief explanation of correct answer + add to `notes.md`
6. **After each domain** — update `progress.md` with score and assessment date
7. **Track per-objective** — map each question to its specific objective number
8. **Keep it engaging** — vary question difficulty, use real-world scenarios, acknowledge good answers
9. **No option descriptions** — answer options should be short labels only, no explanatory text. The real exam doesn't hand-hold with descriptions. Descriptions make educated guessing too easy.
10. **Ask confidence BEFORE revealing the answer** — "Knew it cold / Reasoned it out / Educated guess / Lucky guess". Ask confidence immediately after the user answers, BEFORE saying whether they're right or wrong. Don't count lucky guesses as strong knowledge.
11. **CRITICAL: No priming** — This rule includes ALL of the following violations:
    - **Do NOT announce what topic you're about to test** ("Let me test CASB now", "Switching to ports"). Just ask the question cold.
    - **Do NOT explain a concept and then immediately quiz on it.** If you just taught the CASB/SWG/ZTNA distinction, do NOT ask a CASB question next. Interleave at least 2-3 unrelated questions first.
    - **Do NOT use the answer term in the question stem.** If the answer is "replay attack," the scenario cannot contain the word "replays." If the answer is "firewall logs," the scenario cannot say "the analyst reviewed the firewall logs."
    - **Do NOT use synonyms or obvious restatements of the answer** in the question stem.
    - Mix up topics so the user can't predict what's coming next. Every question should feel cold.
12. **Teach decision rules on wrong answers** — after a miss, explain the distinguishing pattern that reliably points to the correct answer on exam day. Save these to `notes.md`.

### Scoring per objective:
- **Strong** (80%+): Consistently correct, understands nuance
- **Moderate** (50-79%): Gets basics, misses details
- **Weak** (<50%): Needs focused study
- **Not assessed**: No questions asked yet

## Branch Rule

All Security+ study materials live on the `secplus` branch ONLY. Never merge to main. When studying is complete and the exam is passed, delete the branch and all evidence:
```bash
git push origin --delete secplus
git branch -D secplus
```

## File Purposes

| File | Purpose | Updated when |
|------|---------|-------------|
| `CLAUDE.md` | This file — session bootstrap, phase tracking | Phase changes |
| `AGENTS.md` | Agent workflows for content maintenance (gap analysis, builders, validators) | When workflows change |
| `progress.md` | Knowledge map, per-objective scores | After each domain assessment |
| `notes.md` | Running study notes, mnemonics, corrections | After each wrong answer |
| `sessions.md` | Session log with dates and outcomes | End of each session |
| `concept-walkthrough.md` | Reference guide for persistent concept gaps | As needed |
| `glossary.md` | Comprehensive reference — 47 sections, all 5 domains, with decision rules | As needed |
