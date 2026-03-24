# Skill Evals

These are lightweight manual eval cases for every skill in this pack, plus two end-to-end path checks.

## Included eval files
- `research-plan.md`
- `research-documentation.md`
- `paper-triage.md`
- `benchmark-verification.md`
- `experiment-setup.md`
- `experiment-log.md`
- `results-analysis.md`
- `results-report.md`
- `verification-protocol.md`
- `research-review.md`
- `end-to-end.md`

## How to use
1. Start Codex with this repository loaded.
2. Give one prompt from a skill eval file.
3. Check whether the skill triggers and whether the output satisfies the acceptance criteria.
4. Record failures before editing the skill.
5. Re-run the same case after changes.

## Scoring suggestion
- pass
- partial
- fail

Track two things separately:
- trigger quality: did the correct skill activate?
- execution quality: did the skill ask, write, and stop correctly?
