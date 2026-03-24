---
name: results-report
description: Turn research artifacts, experiment logs, and analysis outputs into a concise, decision-oriented AI/ML research report. Use when the user needs the best supported conclusion, what not to trust yet, the practical takeaway, and the next actions that still require approval.
---

# Results Report

Write the decision memo after the analysis is done.

## Core objective
Produce `research/results_report.md` that a human can use to decide what to do next.

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
3. Summarize the best current result relative to baseline or control when experiments exist. Otherwise, summarize the best supported literature conclusion.
4. Include important failures, regressions, and contradictory evidence that changed the path.
5. End with recommended next actions and mark which ones require approval.
6. Preserve the canonical shared report schema. Update relevant sections instead of replacing the file with an incompatible experiment-only format.
7. Do not hide uncertainty to make the report sound stronger.

## Reporting rules
- Tie claims to experiment IDs, source rows, and analysis artifacts.
- Do not upgrade exploratory evidence into a final recommendation.
- If verification is incomplete, say so in the executive summary.
- Quantify compute or run budget usage when it changes the practical recommendation.
- Make stop / continue / pivot recommendations explicit.
- If no experiments exist, say `N/A` rather than inventing experiment outcomes.

## Output structure
Use this order:
- Executive summary
- Scope and method
- Best-supported findings
- Benchmark and experiment notes
- Important negative evidence or risks
- Open questions and unresolved risks
- Recommended next actions
- Evidence links

## References and templates
- Use `assets/results-report-template.md`.
- Use `references/report-checklist.md`.
