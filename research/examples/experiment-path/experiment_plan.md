# Experiment Plan

## Research Scope Reference
- Related research question: Does LoRA rank 16 improve validation F1 relative to rank 8?
- Linked `active-plan.md` sections: sections 1, 3, 7, and 10

## Current Approved Step
- Objective: confirm the rank 8 baseline as E000
- Comparison target: current production config
- Single variable to test or confirm: none for E000; baseline confirmation only
- Why this step is next: later ablations are uninterpretable until the baseline is pinned

## Planned Steps
1. confirm the exact baseline config and eval command
2. run approved E000 baseline
3. stop for review before E001 rank-16 ablation

## Expected Outputs
- Proposed experiment ID: E000
- Metrics or artifacts to produce: validation F1, log file, experiment entry
- Files likely to change: none before approval

## Risks or Blockers
- OOM risk if hidden config drift occurred

## Approval Checklist
- Baseline run approved? yes
- Code change approved? no
- Long job approved? yes
- Scope change approved? no
