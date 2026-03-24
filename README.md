# Semi-autonomous Codex Research Pack

This pack is a Codex-native starter for semi-autonomous AI/ML research. It keeps the human in the loop and adds a lean experimental workflow on top of the earlier plan / documentation / review skills.

## Assumptions
- Runtime: Codex CLI / Codex-compatible skills
- Operating style: human-in-the-loop, not full autonomy
- Research domain: ML/AI papers, repos, benchmarks, model cards, eval claims, and small-to-medium experiment workflows
- External APIs: not assumed
- Default posture: ask before broad search, installs, baseline runs, experiments, or network-heavy work

## Install
Unzip this archive at the root of the repository you want Codex to use. The important paths are:
- `AGENTS.md`
- `.agents/skills/...`

Codex will read `AGENTS.md` before work starts and discover skills from `.agents/skills`.

## Recommended starting mode
```bash
codex --sandbox read-only --ask-for-approval on-request
```

## Suggested first prompt
```text
Read AGENTS.md. Use research-plan to scope the task with me. If experiments are likely, hand off to experiment-setup and wait for my approval before any baseline run or code changes.
```

## Files included

### Core research skills
- `research-plan`
- `research-documentation`
- `research-review`
- `paper-triage`
- `benchmark-verification`

### Core experimental additions
- `experiment-setup`
- `experiment-log`
- `results-analysis`
- `results-report`
- `verification-protocol`

## Intended operating loop
1. scope the task with `research-plan`
2. define the experiment contract with `experiment-setup`
3. run only approved work
4. record every run with `experiment-log`
5. analyze outputs with `results-analysis`
6. verify nontrivial claims with `verification-protocol`
7. write the decision memo with `results-report`
8. red-team the conclusion with `research-review`

## What this pack intentionally does **not** assume
- external APIs
- Zotero or Obsidian
- Docker / Apptainer
- cloud schedulers
- a specific ML framework beyond ordinary repo-local commands

## What to customize next
1. default deliverable type
2. preferred evaluation stack and repo commands
3. strictness around benchmark evidence
4. whether to add a dedicated reproduction-planning skill later
