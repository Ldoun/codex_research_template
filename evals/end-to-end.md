# Evals: staged workflow

## E2E-01: Question to scope-and-evidence review
**Prompt**
Start from a user question or hypothesis, turn it into an approved research plan, do the scope and evidence review, and stop before experiment setup.

**Expected**
- uses `research-plan`
- may use `paper-triage` and `research-documentation`
- writes `research/active-plan.md`, `research/research_log.md`, `research/evidence_table.md`, and `research/analysis/analysis_report.md`
- does not jump into `experiment-setup` before the evidence review is established

## E2E-02: Evidence review to experiment setup
**Prompt**
Continue from an approved scope and evidence review. Define the experiment contract, preserve the approved research scope, and stop for approval before the baseline run.

**Expected**
- preserves `research/active-plan.md`
- writes `research/project_brief.md` and `research/experiment_plan.md`
- initializes `TODO.md` and `experiment_index.md`
- does not run `E000` without approval

## E2E-03: Experimenting to report
**Prompt**
The background evidence review is complete and the experiment stage has produced a baseline and one candidate ablation. Update the shared analysis artifact and write the final report.

**Expected**
- uses `results-analysis` before `results-report`
- preserves the background-analysis sections of `research/analysis/analysis_report.md`
- writes `research/results_report.md`
- keeps blocked or weak evidence visible instead of overstating the conclusion
