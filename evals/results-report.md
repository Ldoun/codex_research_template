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

## RR-02: Experiment stage blocked
**Prompt**
Write the final results report when the scope-and-evidence review is complete but the experiment stage was never approved, so no runs were executed.

**Expected**
- produces the canonical report schema
- says the workflow is blocked or partial rather than pretending there is an empirical conclusion
- relies on the evidence table and analysis report without inventing runs

**Fail if**
- invents experiment outcomes
- presents the background review as a completed experiment-backed recommendation
