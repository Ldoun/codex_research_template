---
name: research-review
description: Critically review research plans, logs, experiment records, analysis bundles, verification logs, or final reports for scope drift, weak claim-to-source mapping, benchmark comparability problems, experiment-integrity failures, and unresolved uncertainty. Use when the user wants QA, peer-review-style critique, or a red-team pass before accepting conclusions.
---

# Research Review

Review the work like a skeptical but constructive research lead.

## Core objective
Decide whether the current research artifact is ready to trust, needs revision, or is blocked by missing evidence.

## What to review
Review whichever artifacts exist and matter for the current stage:
- `research/active-plan.md`
- `research/project_brief.md`
- `research/research_log.md`
- `research/evidence_table.md`
- `research/experiment_index.md`
- `research/experiments/*.md`
- `research/analysis/analysis_report.md`
- `research/results_report.md`
- `research/verification_log.md`
- `research/review_notes.md`

Do not require all of them if the task is earlier-stage.

## Review dimensions
1. Scope alignment
2. Claim-to-source traceability
3. Source quality and staleness
4. Missing counterarguments or counterevidence
5. Benchmark comparability
6. Experiment integrity and confounds
7. Reproducibility and implementation realism
8. Verification coverage
9. Hidden assumptions
10. Missing user approvals
11. Recommendation quality

## Output format
Write the review in this order:
- Overall verdict: approve / approve with conditions / not ready
- Blocking issues
- Non-blocking issues
- Missing evidence
- Questions for the user
- Recommended next steps

## Review rules
- Quote or point to the exact weak claim or artifact gap when possible.
- Distinguish evidence gaps from writing problems.
- Do not rewrite the entire report unless asked; diagnose first.
- Flag benchmark tables that compare non-equivalent settings.
- Flag experiment conclusions that changed more than one variable at once.
- If the report relies on weak sources or unverified claims, say so directly.
- If the workflow skipped a required approval gate, mark it clearly.

## References and templates
- Use `references/review-checklist.md` for the full rubric.
- Use `assets/review-notes-template.md` when writing `research/review_notes.md`.
