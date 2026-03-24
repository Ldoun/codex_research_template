# Semi-autonomous Codex Research Pack (Template + Enforcement)

This pack keeps the broader semi-autonomous AI/ML research template and adds a lean enforcement layer: a short root `AGENTS.md`, stage-specific research skills, canonical artifacts, starter research directories, and lightweight manual evals.

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
Read AGENTS.md and summarize the loaded skills. Start from my question or hypothesis, turn it into an approved scope with research-plan, do the background evidence review, then stop for my approval before experiment setup or any baseline run.
```

## Workflow stages

### 1. User question / hypothesis
- `research-plan` turns the user's question or hypothesis into an approved scope contract.

### 2. Scope and evidence review
- `paper-triage` narrows noisy source sets.
- `benchmark-verification` checks benchmark comparability before claims are trusted.
- `research-documentation` maintains the durable background research analysis.

### 3. Experimenting
- `experiment-setup` defines the experiment contract after the evidence review.
- `experiment-log` records each approved run.
- `results-analysis` updates the experiment-analysis sections of the shared analysis artifact.
- `verification-protocol` verifies important empirical or algorithmic claims.

### 4. Report
- `results-report` writes the integrated final report.
- `research-review` red-teams the conclusions before acceptance.

### Supporting structure
- `evals/` for lightweight manual skill checks
- `research/` starter folders for durable artifacts

## Canonical artifact contract
- `research/active-plan.md`: long-lived approved question/hypothesis and scope contract. Only `research-plan` owns this schema.
- `research/project_brief.md`: experiment contract with metric, eval command, baseline, constraints, and budget.
- `research/experiment_plan.md`: current approved experiment step. `experiment-setup` owns this schema.
- `research/analysis/analysis_report.md`: background research analysis that begins in the evidence-review stage and is extended during experimentation.
- `research/results_report.md`: final integrated report. `results-report` owns this schema.

The analysis artifact is shared across the evidence-review and experimentation stages so background findings and empirical findings stay in one traceable place.

## Intended operating workflow

### Stage 1. User question / hypothesis
1. clarify the exact question or hypothesis
2. resolve the deliverable, seed sources, constraints, and approval boundaries
3. write the approved scope contract with `research-plan`

### Stage 2. Scope and evidence review
1. triage sources if the candidate set is noisy
2. collect traceable evidence and benchmark-comparability notes
3. maintain `research/research_log.md`, `research/evidence_table.md`, and `research/analysis/analysis_report.md`
4. stop when the background analysis is strong enough to justify experiment design

### Stage 3. Experimenting
1. convert the approved scope and evidence review into `research/project_brief.md` and `research/experiment_plan.md`
2. wait for approval before the baseline run or any metric-driven code change
3. log every approved run with `experiment-log`
4. update the shared analysis artifact with `results-analysis`
5. verify important claims with `verification-protocol`

### Stage 4. Report
1. write `research/results_report.md` with `results-report`
2. red-team the report with `research-review`
3. stop with explicit established / uncertain / needs approval sections

For AI/ML work, this template expects background evidence review to feed experimentation rather than act as a separate terminal path by default.

## Design intent
- Human in the loop
- Codex-native
- No API dependency assumed
- No container, database, or external knowledge tool required by default
- Research quality and traceability matter more than autonomy
