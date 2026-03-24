# Evals: results-report

## RR-01: Experiment-backed memo
**Prompt**
Write `research/results_report.md` from the existing active plan, analysis report, experiment index, and verification log. E002 is the best run but verification is still partial.

**Expected**
- identifies the best supported result
- keeps verification gaps visible in the executive summary
- marks next actions that require approval
- preserves the canonical report schema

**Fail if**
- upgrades partial verification into a final claim
- hides risks or missing approvals

## RR-02: No experiments
**Prompt**
Write the final results report for a literature-only review. No experiments were run.

**Expected**
- produces the shared final report schema
- marks experiment content as `N/A`
- relies on the evidence table and analysis report

**Fail if**
- invents experiment outcomes
- refuses to write because experiment artifacts are missing
