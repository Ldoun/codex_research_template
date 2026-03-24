# Results Report

## Executive Summary
- Decision or bottom line: The baseline is confirmed; approve one single-variable E001 ablation at LoRA rank 16 if further experimentation is desired.
- Confidence: medium
- One-sentence reason: E000 is decision-grade for baseline confirmation, but no improvement claim can be made before E001 exists.

## Scope and Method
- Approved scope: baseline confirmation followed by at most one rank-only ablation
- Sources used: internal repo docs and config inspection
- Experiments included: E000
- Important exclusions: no rank-16 run yet

## Best-Supported Findings
- Finding 1: E000 reproduces the approved baseline at 88.4 F1.
- Evidence links: `experiment_index.md`, `experiments/E000.md`, `analysis/analysis_report.md`, `verification_log.md`
- Caveats: this is not evidence that rank 16 improves performance.

## Benchmark and Experiment Notes
- Best verified benchmark interpretation: internal validation F1 is currently pinned for the baseline only.
- Best experiment result or `N/A`: E000 = 88.4 F1 baseline confirmation
- Comparison caveats: no candidate ablation has been run yet

## Important Negative Evidence or Risks
- No improvement evidence exists yet.
- Memory pressure could confound the next run if rank 16 changes hidden settings.

## Open Questions and Unresolved Risks
- Is one full E001 run sufficient, or is a seed sweep required?
- Can rank 16 be tested without touching batch size or other settings?

## Recommended Next Actions
1. Approve E001 with LoRA rank 16 only.
2. Keep preprocessing and all other settings fixed.
3. Review E001 before any further ablations.

For each action:
- expected value: clean causal evidence for the rank change
- approval required? yes

## Evidence Links
- Active plan: `active-plan.md`
- Project brief: `project_brief.md`
- Research log: `research_log.md`
- Evidence table: `evidence_table.md`
- Analysis report: `analysis/analysis_report.md`
- Verification log: `verification_log.md`
- Experiment index: `experiment_index.md`
