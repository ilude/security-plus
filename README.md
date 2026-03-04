# Security+ SY0-701 Study System

A structured study system for the CompTIA Security+ SY0-701 exam, designed to be used with [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

## How It Works

Claude Code reads the `CLAUDE.md` file in this repo as its instruction set. It acts as an adaptive tutor that:

- **Assesses** your knowledge across all 5 exam domains with scenario-based questions
- **Tracks** per-objective scores in `progress.md` so you always know where you stand
- **Drills** weak areas with exam-realistic questions (4 options, no hand-holding descriptions)
- **Teaches** decision rules when you get answers wrong — patterns that distinguish similar concepts
- **Logs** every session to `sessions.md` so you can pick up where you left off

Questions match the real exam format: scenario-based stems, plausible distractors, bare acronyms. A confidence check after each answer prevents lucky guesses from masking gaps.

> **Note on PBQs**: The real Security+ exam includes Performance-Based Questions — interactive simulations like configuring a firewall, matching items, or completing a network diagram. This system attempts to approximate PBQ-style thinking with scenario questions, but it is fundamentally a **multiple-choice study tool**. It cannot replicate drag-and-drop, interactive labs, or hands-on simulations. For PBQ practice, supplement with lab environments or dedicated PBQ trainers.

## Getting Started

1. Clone this repo
2. Open the directory in Claude Code (`claude` in terminal)
3. Say "begin" — Claude will ask about your background, then launch a 25-question baseline eval across all 5 domains

## Exam Reference

| | |
|---|---|
| **Exam** | CompTIA Security+ SY0-701 |
| **Format** | 90 questions, 90 minutes |
| **Passing** | 750/900 (~83%) |
| **Types** | Multiple-choice + Performance-Based Questions (PBQs) |

### Domain Weights

| Domain | Weight | Description |
|--------|--------|-------------|
| 4 | 28% | Security Operations |
| 2 | 22% | Threats, Vulnerabilities, and Mitigations |
| 5 | 20% | Security Program Management and Oversight |
| 3 | 18% | Security Architecture |
| 1 | 12% | General Security Concepts |

## File Structure

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Study system instructions — Claude reads this to know how to tutor you |
| `progress.md` | Per-objective scorecard — tracks Strong/Moderate/Weak across all domains |
| `sessions.md` | Session log — date, questions asked, scores, key improvements |
| `notes.md` | Running study notes — wrong answers, decision rules, mnemonics |
| `concept-walkthrough.md` | Reference guide for commonly confused concepts |
| `glossary.md` | Comprehensive reference — 47 sections covering all 5 domains with decision rules, validated against official exam objectives |

## Study Timeline

The system is designed for a 3-day intensive cram, but works at any pace:

- **Day 1**: Assessment across all domains, then drill the weakest areas in the heaviest domains
- **Day 2**: Targeted drilling on gaps, scenario-based questions, acronym drills
- **Day 3**: Practice exam, review misses, final cram

## Customization

Edit `CLAUDE.md` to adjust:

- **Study Timeline** — change the 3-day structure to fit your schedule
- **Quiz Instructions** — tweak question format, confidence tracking, or explanation style

The User Knowledge Profile is collected automatically via conversation on first launch — no file editing needed.

## License

MIT
