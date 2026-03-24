---
name: experiment-setup
description: Define the experiment contract for semi-autonomous AI/ML research before any baseline run, ablation, reproduction, or metric-driven code change. Use when experiments may happen and Codex must ask the right questions, pin down the metric and eval command, capture constraints and compute budget, draft the project brief and experiment plan, and stop for approval before execution.
---

# Experiment Setup

Set the experiment contract before touching the metric.

## Core objective
Produce an approved `research/project_brief.md` and an approved `research/experiment_plan.md` that tell Codex exactly what counts as progress, what is fixed, and what requires approval.

## When to trigger
Trigger when the user asks for:
- a baseline run
- an ablation
- a benchmark or reproduction
- a code change intended to improve a metric
- experiment planning for an AI/ML question

Do not trigger for purely literature-only work unless the user expands scope toward experiments.

## Required workflow
1. Read the current `research/active-plan.md`, if present, and the user's latest approved scope.
2. Ask only the missing questions, grouped into short rounds:
   - goal and deliverable
   - primary metric and exact evaluation command
   - current baseline and fixed constraints
   - preferred approaches, references, and off-limits files
   - compute budget, minimum decision scale, and approval boundaries
3. Resolve or explicitly mark `TBD` for:
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
4. Draft `research/project_brief.md` in chat first using `assets/project-brief-template.md`.
5. Draft `research/experiment_plan.md` in chat first using `assets/experiment-plan-template.md`.
6. Show both drafts back to the user for review.
7. Ask whether anything should be changed.
8. Only after approval:
   - save `research/project_brief.md`
   - save `research/experiment_plan.md`
   - initialize `research/TODO.md`
   - initialize `research/experiment_index.md`
   - propose the baseline run as `E000`
9. Preserve the schema and role of `research/active-plan.md`. Only update it if the user explicitly changes the approved research scope.
10. Stop and wait for approval before running the baseline or making metric-driven code changes.

## Setup rules
- If the evaluation command is unclear, do not guess; surface the ambiguity.
- If the baseline is unknown, record it as `TBD` and propose a baseline-confirmation step.
- If the user gives multiple ideas, separate:
  - approved now
  - later options
  - explicitly out of scope
- Keep the setup inspectable. Never convert it into hidden autonomy.
- If the task is blocked on missing information, say exactly what is missing.
- Do not run anything yet.

## Output
Produce:
- a draft or saved `research/project_brief.md`
- a draft or saved `research/experiment_plan.md`
- a proposed baseline `E000` objective
- a short list of what still needs approval

## References and templates
- Use `assets/project-brief-template.md`.
- Use `assets/experiment-plan-template.md`.
- Use `assets/todo-template.md` when initializing `research/TODO.md`.
- Use `assets/experiment-index-template.md` when initializing `research/experiment_index.md`.
- Use `references/setup-checklist.md` when deciding what is still missing.
