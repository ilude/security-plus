# Security+ SY0-701 Study System

## Quick Start

When starting a study session, read these files in order:
1. This file (context + instructions)
2. `progress.md` (current knowledge map)
3. `sessions.md` (last session recap)
4. `notes.md` (accumulated knowledge)

Then pick up where we left off based on current phase.

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

### Day 1: Assessment + Triage
- Rapid assessment: ~3-5 questions per domain (heaviest domains first)
- Record scores to `progress.md` immediately after each domain
- After full assessment, drill weakest areas in heaviest domains

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

<!-- Fill this in at the start of your study. This helps Claude calibrate question difficulty and focus areas. -->

- **IT experience level**: (e.g., 5 years sysadmin, 10 years developer, fresh grad)
- **Known strengths**: (e.g., networking, Linux, cloud, scripting)
- **Known weaknesses**: (e.g., cryptography, compliance frameworks, newer cloud acronyms)
- **Exam-specific notes**: (e.g., "I know concepts but not the acronym names", "first attempt", "retake after failing with 720")

## Current Phase

**Phase**: Day 1 — Not started
**Status**: Begin with assessment
**Next action**: Start Domain 4 assessment (highest weight)

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

### Domain assessment order (heaviest weight first):
1. Domain 4: Security Operations (28%)
2. Domain 2: Threats, Vulnerabilities, and Mitigations (22%)
3. Domain 5: Security Program Management and Oversight (20%)
4. Domain 3: Security Architecture (18%)
5. Domain 1: General Security Concepts (12%)

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
| `progress.md` | Knowledge map, per-objective scores | After each domain assessment |
| `notes.md` | Running study notes, mnemonics, corrections | After each wrong answer |
| `sessions.md` | Session log with dates and outcomes | End of each session |
| `concept-walkthrough.md` | Reference guide for persistent concept gaps | As needed |
| `glossary.md` | Acronym and term reference | As needed |
