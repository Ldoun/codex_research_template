---
name: results-analysis
description: Produce a strict post-run analysis bundle from experiment logs, metrics, and artifacts. Use when comparing runs, generating tables or figures, checking whether differences look meaningful, or separating real signal from exploratory noise before writing conclusions.
---

# Results Analysis

Analyze first. Recommend second.

## Core objective
Turn raw experiment outputs into an auditable analysis bundle that distinguishes verified signal from exploratory observations.

## Required workflow
1. Identify the comparison set:
   - baseline / control
   - candidate runs
   - relevant experiment IDs
2. Confirm comparability before analyzing:
   - same metric
   - same dataset / split
   - same evaluation command or a documented reason for difference
   - same decision scale
3. Read the relevant experiment entries and raw output locations.
4. Compute or summarize:
   - per-run metrics
   - deltas vs baseline or control
   - failure rates or instability
   - seed coverage / sample size / confidence caveats
5. Generate or specify the analysis artifacts:
   - `research/analysis/analysis_report.md`
   - `research/analysis/stats_appendix.md`
   - `research/analysis/figure_catalog.md`
6. Explicitly label:
   - likely real signal
   - exploratory hints
   - non-comparable results
   - unresolved measurement issues
7. Stop before the final recommendation; hand off to `results-report`.

## Analysis rules
- Do not call a result “better” until the comparison is direct.
- If the run count or seed coverage is weak, say the evidence is exploratory.
- Separate:
  - observed metric difference
  - statistical or practical importance
  - causal interpretation
- Keep negative results visible.
- Prefer simple, defensible figures over decorative plots.
- If a figure cannot be generated, specify exactly what should be plotted and from which files.

## Output
The analysis bundle should answer:
- What was compared?
- Which comparisons are valid?
- What improved, regressed, or failed?
- How strong is the evidence?
- What still needs verification?

## References and templates
- Use `assets/analysis-report-template.md`.
- Use `assets/stats-appendix-template.md`.
- Use `assets/figure-catalog-template.md`.
- Use `references/analysis-checklist.md`.
