---
name: experiment-setup
description: Define the experiment contract for semi-autonomous AI/ML research before any baseline run, ablation, reproduction, or metric-driven code change. Use when experiments may happen and the user needs Codex to ask the right questions, pin down the metric and eval command, capture constraints and compute budget, and stop for approval before execution.
---

# Experiment Setup

Set the experiment contract before touching the metric.

## Core objective
Produce an approved `research/project_brief.md` that tells Codex exactly what counts as progress, what is fixed, and what requires approval.

## Required workflow
1. Read the current plan and the user’s latest approved scope.
2. Ask only the missing questions, grouped into short rounds:
   - goal and deliverable
   - primary metric and exact evaluation command
   - current baseline and fixed constraints
   - preferred approaches, references, off-limits files
   - compute budget and minimum decision scale
3. Draft the project brief in chat first using `assets/project-brief-template.md`.
4. Show the draft back to the user for review.
5. Ask whether anything should be changed.
6. Only after approval:
   - save `research/project_brief.md`
   - initialize `research/TODO.md`
   - initialize `research/experiment_index.md`
   - propose the baseline run as `E000`
7. Stop and wait for approval before running the baseline or making metric-driven code changes.

## Questions to resolve
Use these fields unless they are already known:
- research goal
- deliverable type
- seed sources or starting code paths
- primary metric and direction
- exact evaluation command
- current baseline
- fixed constraints protected from drift
- minimum decision scale for conclusions
- preferred approaches to try
- references to follow
- off-limits files
- compute / runtime budget
- approval boundaries

## Setup rules
- If the evaluation command is unclear, do not guess; surface the ambiguity.
- If the baseline is unknown, record it as `TBD` and propose a baseline-confirmation step.
- If the user gives multiple ideas, separate:
  - approved now
  - later options
  - explicitly out of scope
- Do not run anything yet.
- Do not turn setup into a hidden autonomous plan; keep it inspectable.

## Output
Produce:
- a draft or saved `research/project_brief.md`
- a proposed baseline `E000` objective
- a short list of what still needs approval

## References and templates
- Use `assets/project-brief-template.md`.
- Use `assets/todo-template.md` when initializing `research/TODO.md`.
- Use `assets/experiment-index-template.md` when initializing `research/experiment_index.md`.
- Use `references/setup-checklist.md` when deciding what is still missing.
