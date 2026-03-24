# Analysis Report

## Task Context
- Research question or decision: Does LoRA rank 16 improve validation F1 relative to the current rank 8 baseline?
- Deliverable type: decision memo
- Current stage: experiment
- Last updated: 2026-03-24

## Sources and Artifacts Reviewed
- Papers / repos / model cards / benchmark docs: internal repo docs, original LoRA paper
- Experiment artifacts included: E000
- Important exclusions: no rank-16 run yet

## Evidence Summary
- Established findings: E000 confirms the baseline at 88.4 F1 on the approved validation command.
- Conflicting findings: none yet
- Open questions: whether E001 rank 16 improves F1 without confounds

## Benchmark and Comparability Notes
- Comparable claims: future E001 can compare directly if it changes LoRA rank only
- Partially comparable claims: any run that changes memory-related settings would need extra caveats
- Non-comparable claims: none yet

## Experiment Comparison Summary
| Experiment | Objective | Eval tier | Metric | Delta vs baseline | Comparable? | Notes |
|---|---|---|---|---|---|---|
| E000 | confirm baseline | full | 88.4 F1 | 0 | yes | baseline pinned |

## Interpretation
- Likely real signal: the baseline is stable enough to support a single-variable ablation next.
- Exploratory hints only: none yet
- Non-comparable or low-confidence items: none yet

## Remaining Verification Needs
- verify that E001 changes LoRA rank only
- decide whether a seed sweep is required after E001
