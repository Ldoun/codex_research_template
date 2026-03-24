# Semi-autonomous Codex Research Pack (Template + Enforcement)

This pack keeps the broader semi-autonomous AI/ML research template and adds a lean enforcement layer: a short root `AGENTS.md`, enforcement-heavy experimental skills, canonical shared artifacts, starter research directories, golden examples, and lightweight manual evals.

## Assumptions
- Runtime: Codex CLI / Codex-compatible skills
- Operating style: human in the loop, not full autonomy
- Research domain: AI/ML papers, repos, benchmarks, model cards, eval claims, and small-to-medium experiment workflows
- External APIs: not assumed
- Default posture: ask before broad search, installs, baseline runs, experiments, or network-heavy work

## Install
Unzip this archive at the root of the repository you want Codex to use. The important paths are:
- `AGENTS.md`
- `.agents/skills/...`
- `evals/...`
- `research/...`

Codex will read `AGENTS.md` before work starts and discover skills from `.agents/skills`.

## Recommended starting mode
```bash
codex --sandbox read-only --ask-for-approval on-request
```

## Suggested first prompt
```text
Read AGENTS.md and summarize the loaded skills. Use research-plan to scope the task with me. If experiments are in scope, hand off to experiment-setup and wait for my approval before any baseline run or code changes.
```

## Skill groups

### Planning and evidence skills
- `research-plan`
- `research-documentation`
- `research-review`
- `paper-triage`
- `benchmark-verification`

### Enforcement-heavy experimental skills
- `experiment-setup`
- `experiment-log`
- `results-analysis`
- `results-report`
- `verification-protocol`

### Supporting structure
- `evals/` for lightweight manual skill checks
- `research/examples/` for end-to-end golden examples
- `research/` starter folders for durable artifacts

## Canonical artifact contract
- `research/active-plan.md`: long-lived approved scope contract for source-heavy work. Only `research-plan` owns this schema.
- `research/project_brief.md`: experiment contract with metric, eval command, baseline, constraints, and budget.
- `research/experiment_plan.md`: current approved experiment step. `experiment-setup` owns this schema.
- `research/analysis/analysis_report.md`: shared analysis artifact used by literature-only and experiment paths.
- `research/results_report.md`: shared final deliverable used by literature-only and experiment paths.

The shared analysis and final report files use a single schema so literature work and experiment work can contribute without clobbering one another.

## Intended operating loops

### Literature-only loop
1. scope the task with `research-plan`
2. use `paper-triage` if the source set is noisy
3. record findings with `research-documentation`
4. use `benchmark-verification` for benchmark-sensitive claims
5. optionally use `verification-protocol` for high-stakes nontrivial claims
6. red-team the conclusion with `research-review`

### Experiment-bearing loop
1. scope the task with `research-plan`
2. define the experiment contract with `experiment-setup`
3. run only approved work
4. record every run with `experiment-log`
5. analyze outputs with `results-analysis`
6. verify nontrivial claims with `verification-protocol`
7. write the decision memo with `results-report`
8. red-team the conclusion with `research-review`

Literature-only work must not be forced through `experiment-setup`.

## Golden examples
See `research/examples/literature-only/` and `research/examples/experiment-path/` for canonical artifact shapes that later skills and resume behavior can consume.

## Design intent
- Human in the loop
- Codex-native
- No API dependency assumed
- No container, database, or external knowledge tool required by default
- Research quality and traceability matter more than autonomy
