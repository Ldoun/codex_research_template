---
name: results-report
description: Turn experiment logs and analysis artifacts into a concise, decision-oriented AI/ML research report. Use when the user needs the best verified result, what not to trust yet, the practical takeaway, and the next actions that still require approval.
---

# Results Report

Write the decision memo after the analysis is done.

## Core objective
Produce `research/results_report.md` that a human can use to decide what to do next.

## Required workflow
1. Read:
   - `research/project_brief.md`
   - `research/experiment_index.md`
   - `research/analysis/analysis_report.md`
   - `research/verification_log.md`, if present
2. Separate:
   - verified findings
   - tentative or exploratory findings
   - unresolved risks
3. Summarize the best current result relative to baseline or control.
4. Include important failures and regressions that changed the path.
5. End with recommended next actions and mark which ones require approval.
6. Do not hide uncertainty to make the report sound stronger.

## Reporting rules
- Tie claims to experiment IDs and analysis artifacts.
- Do not upgrade exploratory evidence into a final recommendation.
- If verification is incomplete, say so in the executive summary.
- Quantify compute or run budget usage when it changes the practical recommendation.
- Make “stop / continue / pivot” recommendations explicit.

## Output structure
Use this order:
- Executive summary
- Best verified result
- What changed relative to baseline
- Important negative results
- Risks, caveats, and unresolved questions
- Recommended next actions
- Evidence links

## References and templates
- Use `assets/results-report-template.md`.
- Use `references/report-checklist.md`.
