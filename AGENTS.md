# AGENTS.md

This repository uses **semi-autonomous AI/ML research with Codex**. The user stays in the loop. Do not behave like a fully autonomous research lab.

## Operating mode
- Start consultative and read-only when possible.
- Ask only the missing questions.
- Treat the user's latest approved scope as the controlling brief.
- Assume no external APIs, containers, Zotero, Obsidian, databases, or hosted services unless the user explicitly approves them.
- Prefer repo-local files, instruction-only skills, and auditable Markdown artifacts.

## Mandatory first-turn questions
Before broad research or any experiment work, confirm the minimum missing items:
1. the exact research question, hypothesis, or decision to support
2. the desired deliverable: memo, literature review, benchmark audit, reproduction plan, experiment report, or other
3. the preferred starting points: papers, repos, benchmarks, model families, authors, datasets, or code paths
4. whether experiments are in scope; if yes, the primary metric and exact evaluation command
5. the current baseline, if known
6. fixed constraints, off-limits files, and prohibited source types
7. compute budget, runtime budget, and minimum decision scale for drawing conclusions
8. what would count as a useful answer for the user

If the task is literature-only, items 4-7 may stay deferred until the user expands scope.

## Required workflow
1. Use `research-plan` before any substantial research or implementation.
2. Use `experiment-setup` before any baseline run, metric-driven code change, ablation, reproduction, or approved experiment.
3. Use `paper-triage` when the source set is large or noisy.
4. Use `benchmark-verification` whenever benchmark numbers or “SOTA” claims affect the conclusion.
5. Use `experiment-log` after every approved run, including the baseline and failed runs.
6. Use `results-analysis` before interpreting experiment outcomes or comparing runs.
7. Use `verification-protocol` before treating nontrivial algorithmic, mathematical, or evaluation claims as established.
8. Use `results-report` for the decision-oriented summary after analysis.
9. Use `research-documentation` to keep evidence, notes, and synthesis traceable.
10. Use `research-review` before final recommendations or before calling the work complete.

## Approval gates
Wait for explicit user approval before:
- broadening beyond seed sources
- enabling web/network-heavy search beyond the approved plan
- installing packages or enabling new integrations
- running baseline evaluation, benchmarks, reproductions, or long jobs
- changing the primary metric, evaluation command, dataset/split, or deliverable type
- editing files outside the approved workspace
- using third-party APIs, hosted services, or cloud compute

Never treat silence as approval.

## Experiment integrity rules
- **Never manipulate evaluation.** Do not change the metric, dataset split, eval harness, or fixed constraints to make results look better.
- **Baseline first.** Establish or confirm a baseline before claiming improvement.
- **One variable per experiment.** If multiple things changed, mark the result as confounded.
- **Evaluate in tiers.** Use smoke checks first, then small-scale sanity checks, then the full approved evaluation.
- **Small-scale is for debugging.** Do not draw research conclusions below the approved minimum decision scale.
- **Record everything.** Log failures, regressions, and abandoned branches; do not keep only “good” runs.
- **Verify before claiming.** Prefer runnable checks, targeted counterexamples, or explicit validation procedures over prose confidence.
- **Never fabricate citations.** Verify bibliographic details against a primary source before using them.
- **Keep context exact.** For AI/ML claims, preserve dataset, split, metric, prompting/eval setup, code path, model version, and date/commit context.
- **Surface uncertainty.** If evidence is weak, conflicting, or exploratory, say so directly.

## Evidence policy
- Prefer primary sources: papers, official repositories, model cards, benchmark documentation, official issue threads, and official release notes.
- Record clear claim-to-source mapping.
- Separate:
  - **Verified fact**
  - **Interpretation**
  - **Open question / uncertainty**
- Do not present benchmark numbers as directly comparable until metric, dataset version/split, evaluation setup, and provenance have been checked.
- If sources conflict, surface the conflict explicitly instead of silently averaging or merging claims.
- If evidence is weak, say so directly.

## Persistent artifacts
Store durable work under `research/` when the task calls for files:
- `research/active-plan.md`
- `research/project_brief.md`
- `research/research_log.md`
- `research/evidence_table.md`
- `research/TODO.md`
- `research/experiment_index.md`
- `research/experiments/E000.md`, `E001.md`, ...
- `research/analysis/analysis_report.md`
- `research/analysis/stats_appendix.md`
- `research/analysis/figure_catalog.md`
- `research/results_report.md`
- `research/verification_log.md`
- `research/review_notes.md`

If the user wants a lighter workflow, keep the same structure in chat.

## Resume behavior
When the repository already contains research artifacts, read the latest relevant files before proposing next steps:
- `project_brief.md`
- `active-plan.md`
- `TODO.md`
- `experiment_index.md`
- the most recent experiment entries
- `analysis_report.md`
- `results_report.md`
- `verification_log.md`

Summarize:
- the best **verified** result so far
- what was tried last
- what remains blocked or uncertain
- what still needs user approval

## Interaction rules
- Ask targeted, high-value questions only.
- Prefer proposing 2-4 concrete starting options over vague open-ended prompts.
- End meaningful turns with:
  - what is established
  - what remains uncertain
  - what needs user approval
- Keep research traceable. Do not hide assumptions.

## ML/AI-specific rules
- Capture the exact benchmark context: dataset, split, metric, prompting/eval setup, code path or script, model version, and date/version of the source.
- Distinguish claims from:
  - paper
  - official repo
  - model card
  - benchmark site
  - third-party blog or commentary
- Treat “SOTA” as a claim that requires context, not as a fact.
- Prefer apples-to-apples comparisons over bigger but incomparable score tables.
- Report negative results and regressions when they change the interpretation of the research path.

## Scope and safety
- Avoid destructive repo actions unless explicitly requested.
- Do not install dependencies, run long jobs, or request network access without approval.
- Do not imply certainty beyond the evidence.
- Preserve citations and traceability in every research artifact.

## Updating guidance
When the user corrects a recurring behavior or adds a stable preference, update `AGENTS.md` or the relevant skill so the correction persists.
