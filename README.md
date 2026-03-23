# Codex Research Template

This repository is a process template for running research projects with Codex. It is not a runnable project by itself. The main value is the instruction scaffold in `AGENTS.md`, plus a small set of repo-local skills that help initialize, maintain, and review a research workflow.

Edit `.agents/templates/research-base.md` for reusable methodology; edit Section 8 in `AGENTS.md` for project-specific setup.

This template supports one root `AGENTS.md`. Do not create multiple root instruction files; use `.agents/templates/research-base.md` as the reusable source template, and keep project-specific instructions in the single root `AGENTS.md`.

## What This Template Includes

- `AGENTS.md`: the main research operating manual. It defines global constraints, experiment discipline, reporting rules, verification rules, and a project-specific Section 8 that you fill in.
- `.agents/templates/research-base.md`: the base instruction template used to refresh Sections 0-7 while preserving project-specific instructions.
- `.agents/skills/setup_research_plan/SKILL.md`: initializes a new research project or resumes an existing one.
- `.agents/skills/update_base/SKILL.md`: updates the instruction base without overwriting Section 8.
- `.agents/skills/retro/SKILL.md`: appends retrospective notes to `REVISION.md`.
- `.gitignore`: standard Python and environment ignores, including `.venv`.

## Who This Is For

Use this template if you want Codex to act like a disciplined research agent rather than a generic coding assistant. The instructions are aimed at:

- mathematical research
- numerical experiments
- deep learning or GPU-heavy work
- long-running projects that need a persistent experimental record

## Quick Start

1. Open the repository in Codex.
2. Edit `AGENTS.md` and fill in `## 8. Project Instructions`.
3. Add or point to the actual codebase and evaluation command for your project.
4. Ask Codex to use the setup skill.

Example prompt:

```text
Use $setup_research_plan to initialize this repository for my project.
```

Section 8 is the part that makes the template project-specific. At minimum, fill in:

- research goal
- primary metric and whether higher or lower is better
- exact evaluation command
- current baseline
- fixed constraints that must not change
- minimum scale for drawing conclusions
- preferred approaches and references
- compute budget
- off-limits files

## What `$setup_research_plan` Does

The setup skill is the main entry point. It checks the repository state and handles three cases:

- Fresh start: Section 8 still contains placeholders.
- Partial setup: Section 8 is filled in, but `report.tex` does not exist yet.
- Resume: Section 8 is filled in and `report.tex` already exists.

For a fresh or partial setup, the intended workflow is:

1. confirm or gather the missing project instructions
2. inspect the repository
3. run `uv sync` if `pyproject.toml` exists
4. run the baseline evaluation from Section 8
5. create the tracking files and directories
6. begin the experiment loop

This template does not include evaluation code. Your project still needs a real codebase and a real eval command.

## Expected Repository State

A usable project based on this template will usually contain these files over time:

- `AGENTS.md`: the active instruction file
- `report.tex`: the single source of truth for experiments
- `TODO.md`: open questions, deferred work, and unverified claims
- `REVISION.md`: retrospective notes written by `$retro`
- `scripts/verify_*.py`: verification scripts
- `scripts/plot_*.py`: plotting scripts
- `images/`: generated figures
- `references.bib`: bibliography for literature-heavy projects
- `artifacts/` or `logs/`: large outputs such as logs, checkpoints, or generated data

The current repository is intentionally minimal, so most of those files are created later by the workflow.

## Daily Workflow

Once initialized, the template expects each session to follow the same loop:

1. read `report.tex`
2. read `TODO.md`
3. read the project instructions in Section 8
4. check recent git history and working tree status
5. summarize the best result, latest experiment, and next step
6. continue the next experiment

Each experiment should then follow the same pattern:

1. explore the codebase
2. write down the plan in `report.tex`
3. implement a small change
4. evaluate in tiers
5. analyze the result honestly
6. record the result in `report.tex`
7. update `TODO.md`
8. commit a completed experiment

## Repo-Local Skills

### `$setup_research_plan`

Use this when:

- Section 8 is still placeholder text
- `report.tex` or `TODO.md` does not exist yet
- you want Codex to resume the project from the current state

Example:

```text
Use $setup_research_plan to resume this project and tell me the next experiment.
```

### `$update_base`

Use this when the repo-local base template changed and you want to refresh Sections 0-7 without rewriting your project-specific Section 8.

Example:

```text
Use $update_base to sync the latest base instructions into this repo.
```

### `$retro`

Use this after a research session when you want Codex to review how the workflow went and append improvement notes to `REVISION.md`.

Example:

```text
Use $retro and focus on what should change in the instruction file.
```

## `AGENTS.md` vs `AGENTS.override.md`

The canonical project instruction file is the single root `AGENTS.md`.

The workflow looks for the active instruction file in this order:

1. `AGENTS.override.md`
2. `AGENTS.md`

If both exist, `AGENTS.override.md` takes precedence. Use that only when you intentionally want a temporary higher-priority local override, not as a second long-term root instruction file.

## Core Conventions

The template is opinionated. The most important conventions are:

- use `uv` for Python environment and package management
- do not compile `report.tex`; edit and syntax-check only
- do not manipulate metrics, test sets, or protected constraints
- change one variable per experiment
- evaluate in tiers before full runs
- verify nontrivial claims with code, not just prose
- record every experiment, including failures
- keep large outputs out of the source tree and store them under `artifacts/` or `logs/`

Git conventions are also part of the workflow. The expected commit format is:

```text
exp(EXXX): <description> -- <metric>=<value> (<delta> vs baseline)
```

## Recommended First Prompt

If you want the shortest path from template to active project, use:

```text
Read AGENTS.md, fill in any missing setup details with me, then use $setup_research_plan to initialize the research workflow for this repository.
```

That prompt is enough to turn this minimal template into a tracked research project.
