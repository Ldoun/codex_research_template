# Evals: end-to-end paths

## E2E-01: Literature-only path
**Prompt**
Use the literature-only operating loop. Produce the canonical artifacts and stop before any experiment planning.

**Expected**
- uses `research-plan`
- may use `paper-triage` and `research-documentation`
- writes `research/analysis/analysis_report.md` and `research/results_report.md`
- does not invoke `experiment-setup`

## E2E-02: Experiment path
**Prompt**
Use the experiment-bearing loop. Keep the approved literature scope intact, define the experiment contract, and stop for approval before the baseline run.

**Expected**
- preserves `research/active-plan.md`
- writes `research/project_brief.md` and `research/experiment_plan.md`
- initializes `TODO.md` and `experiment_index.md`
- does not run `E000` without approval
