---
name: experiment-log
description: Record every approved baseline, experiment, ablation, failure, regression, or reproduction attempt as a durable Markdown artifact. Use after any run or code change intended to affect a metric, especially when experiment continuity matters across sessions and the team needs a trustworthy per-run history.
---

# Experiment Log

If a run mattered, it needs an entry.

## Core objective
Create or update durable experiment records that preserve what changed, how it was evaluated, and what happened.

## Required workflow
1. Assign or confirm the experiment ID:
   - `E000` for baseline confirmation
   - `E001`, `E002`, ... for subsequent runs
2. Create or update `research/experiments/EXXX.md` from `assets/experiment-entry-template.md`.
3. Capture the one-line objective and the **single variable changed** relative to the comparison run.
4. Record the exact execution context:
   - command(s)
   - commit / branch / diff summary if known
   - config path or important settings
   - dataset / split
   - metric
   - evaluation tier
   - hardware / runtime context
   - seed(s), if relevant
5. Record the result:
   - status: completed / failed / aborted / partial
   - metric outcome
   - delta vs baseline or control
   - key observations
   - missing outputs or anomalies
   - next action
6. Update `research/experiment_index.md`.
7. Update `research/TODO.md` when the run creates new follow-up work.

## Logging rules
- Log failures and regressions; do not keep only positive runs.
- If multiple variables changed, mark the entry as **confounded**.
- Distinguish evaluation tiers:
  - smoke
  - sanity / subset
  - full
- Do not claim improvement from a smoke or sanity run.
- Keep comparison targets explicit: baseline, control, or previous run.
- If raw outputs are missing, say so rather than reconstructing from memory.

## Output
After logging, provide:
- the experiment ID
- the status
- whether the result is decision-grade or exploratory only
- the recommended next action that still needs approval, if any

## References and templates
- Use `assets/experiment-entry-template.md`.
- Use `assets/experiment-index-template.md`.
- Use `references/logging-checklist.md`.
