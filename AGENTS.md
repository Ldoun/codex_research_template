# AGENTS.md

## Operating mode
- This repository uses semi-autonomous AI/ML research with Codex.
- Keep the user in the loop. Ask targeted questions before broadening scope or running experiments.
- Keep this file short. Put repeatable workflows in skills, not here.
- Assume no external APIs, containers, hosted tools, Zotero, or Obsidian unless the user explicitly approves them.

## Resolve before deep work
Before substantial research or any experiment work, resolve the missing items:
1. exact research question or decision to support
2. desired deliverable
3. approved seed sources, repos, code paths, benchmarks, papers, or authors
4. whether experiments are in scope
5. if experiments are in scope: primary metric, exact evaluation command, and known baseline
6. fixed constraints, off-limits files, and forbidden shortcuts
7. compute or runtime budget and minimum decision scale
8. what still needs explicit approval

## Workflow stages
Use this staged workflow unless the user explicitly narrows the job:
1. user question or hypothesis
2. scope and evidence review
3. experimenting
4. report

## Skill routing
Stage 1: user question or hypothesis
- `research-plan` to turn the user request into the approved scope contract in `research/active-plan.md`

Stage 2: scope and evidence review
- `paper-triage` when candidate sources are noisy or numerous
- `benchmark-verification` when benchmark numbers or "SOTA" claims matter
- `research-documentation` to maintain `research_log.md`, `evidence_table.md`, and `analysis/analysis_report.md`

Stage 3: experimenting
- `experiment-setup` after the scope and background evidence review are strong enough to design an experiment contract
- `experiment-log` after every approved run, including failures and regressions
- `verification-protocol` before treating nontrivial empirical or algorithmic claims as established
- `results-analysis` to update the experiment-analysis sections of `analysis/analysis_report.md`

Stage 4: report
- `results-report` for the final integrated report in `results_report.md`
- `research-review` before accepting conclusions

Do not skip from the initial question directly to experiments unless the user has already approved the required scope, metric, eval command, and constraints.

## Approval gates
Wait for explicit user approval before:
- broadening beyond approved seed sources
- enabling web or network-heavy search beyond the approved plan
- installing packages or enabling new integrations
- running a baseline, benchmark, reproduction, or long job
- changing the metric, evaluation command, dataset or split, or deliverable
- editing files outside the approved workspace
- using third-party APIs, hosted services, or cloud compute

Never treat silence as approval.

## Experiment rules
- Baseline first.
- One variable per experiment; otherwise mark the run confounded.
- Evaluate in tiers: smoke, sanity, then full.
- Small-scale runs are for debugging only, not for conclusions.
- Never manipulate evaluation.
- Log failures and regressions, not only wins.
- Preserve exact context: dataset, split, metric, prompting or eval setup, model version, code path, commit, and date.
- Verify before claiming.
- Never fabricate citations.

## Evidence rules
- Prefer primary sources: papers, official repositories, model cards, benchmark docs, official issues, and release notes.
- Separate verified fact, interpretation, and open question.
- Do not treat benchmark numbers as directly comparable until metric, dataset version or split, evaluation setup, and provenance have been checked.
- Surface conflicts and uncertainty directly.

## Canonical artifacts
Keep durable work under `research/` when the task calls for files:
- `active-plan.md` - long-lived approved question or hypothesis and scope contract owned by `research-plan`
- `project_brief.md` - experiment contract owned by `experiment-setup`
- `experiment_plan.md` - current approved experiment step owned by `experiment-setup`
- `research_log.md`
- `evidence_table.md`
- `TODO.md`
- `experiment_index.md`
- `experiments/E000.md`, `E001.md`, ...
- `analysis/analysis_report.md` - canonical background-analysis and experiment-analysis artifact shared across stages 2 and 3
- `analysis/stats_appendix.md`
- `analysis/figure_catalog.md`
- `results_report.md` - canonical final report owned by `results-report`
- `verification_log.md`
- `review_notes.md`

## Shared-file rules
- Do not let `experiment-setup` overwrite the schema of `active-plan.md`.
- Do not let `research-documentation` and `results-analysis` invent competing schemas for `analysis/analysis_report.md`.
- Do not let any stage before `results-report` treat `results_report.md` as the canonical working document.
- If a shared artifact already exists, update the relevant sections and preserve compatible prior content.

## Resume behavior
On resume, read the latest relevant research artifacts before proposing next steps:
- `active-plan.md`
- `project_brief.md`, if present
- `experiment_plan.md`, if present
- `research_log.md`, if present
- `evidence_table.md`, if present
- `TODO.md`, if present
- `experiment_index.md`, if present
- the most recent experiment entries, if present
- `analysis/analysis_report.md`, if present
- `results_report.md`, if present
- `verification_log.md`, if present

## End-of-turn structure
For meaningful research turns, end with:
- established
- uncertain
- needs approval
