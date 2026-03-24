# Project Brief

## Status
- Draft / Approved: Approved
- Last updated: 2026-03-24
- Owner: user

## Research Goal
- Question / hypothesis: Does LoRA rank 16 improve validation F1 relative to the current rank 8 baseline?
- Desired deliverable: decision memo

## Approved Starting Points
- Papers / repos / benchmarks / code paths: internal repo `train.py`, `eval.py`, `configs/ner/base.yaml`
- Notes: keep preprocessing fixed

## Primary Metric
- Name: validation F1
- Direction (higher/lower is better): higher
- Exact evaluation command: `python eval.py --config configs/ner/base.yaml --split val`
- Baseline: current rank 8 config
- Notes on dataset / split / harness: internal validation split only

## Fixed Constraints
- Protected settings: preprocessing, dataset split, optimizer, prompt template
- Forbidden shortcuts / forbidden sources: no test-set peeking, no external APIs
- Off-limits files: `data_pipeline/*`

## Minimum Decision Scale
- Small-scale runs are for debugging only until: the full validation split is used
- Full-decision threshold: one approved full validation run per condition

## Approach Priorities
1. confirm baseline
2. test rank 16 only
3. stop for review

## References to Follow
- Primary references: internal repo docs, original LoRA paper
- Supporting references: internal dataset card

## Compute Budget
- Max runtime: 2 hours
- Max number of runs: 2 full runs
- Hardware / GPU budget: 1 GPU
- Cost boundary: existing local machine only

## Approval Gates
- Need approval before: any full run, any config change beyond LoRA rank, any extra ablation
- Safe to do without new approval: reading code and drafting artifacts

## Notes
- Risks: rank change could interact with batch size if memory becomes tight
- Open questions: whether a seed sweep is necessary after the first full comparison
