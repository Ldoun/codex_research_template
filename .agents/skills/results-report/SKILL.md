---
name: results-report
description: Turn the approved question or hypothesis, the background evidence review, and the experiment outputs into a concise, decision-oriented AI/ML research report. Use when the user needs the best supported conclusion, what not to trust yet, the practical takeaway, and the next actions that still require approval.
---

# Results Report

Write the decision memo after the analysis is done.

## Core objective
Produce `research/results_report.md` that integrates the evidence-review stage and the experimentation stage into a final decision document.

## Required workflow
1. Read the available canonical artifacts:
   - `research/active-plan.md`
   - `research/project_brief.md`, if present
   - `research/research_log.md`, if present
   - `research/evidence_table.md`, if present
   - `research/analysis/analysis_report.md`
   - `research/experiment_index.md`, if present
   - `research/verification_log.md`, if present
2. Separate:
   - verified findings
   - tentative or exploratory findings
   - unresolved risks
3. Summarize the approved question or hypothesis, the most important evidence-review findings, and the best current experimental result relative to baseline or control.
4. Include important failures, regressions, and contradictory evidence that changed the path.
5. End with recommended next actions and mark which ones require approval.
6. Preserve the canonical report schema. Update relevant sections instead of replacing the file with an incompatible ad hoc format.
7. If experimentation was planned but not completed, say the workflow is blocked or incomplete rather than pretending the background analysis is a final empirical answer.
8. Do not hide uncertainty to make the report sound stronger.

## Reporting rules
- Tie claims to experiment IDs, source rows, and analysis artifacts.
- Do not upgrade exploratory evidence into a final recommendation.
- If verification is incomplete, say so in the executive summary.
- Quantify compute or run budget usage when it changes the practical recommendation.
- Make stop / continue / pivot recommendations explicit.
- If experiments are missing or incomplete, state why and mark the report as blocked or partial rather than inventing outcomes.

## Output structure
Use this order:
- Question / hypothesis
- Executive summary
- Scope and evidence review summary
- Experiment summary
- Best-supported conclusion
- Important negative evidence or risks
- Open questions and unresolved risks
- Recommended next actions
- Evidence links

## References and templates
- Use `assets/results-report-template.md`.
- Use `references/report-checklist.md`.
