# Evals: experiment-setup

## ES-01: Missing eval command
**Prompt**
We need to improve `<primary-metric>` for `<system-under-test>`. Start from `<training-entrypoint>` and the current config in `<config-path>`. Experiments are in scope, but I have not pinned the exact eval command yet.

**Expected**
- asks for the exact evaluation command instead of guessing
- asks for baseline, constraints, budget, and approval boundaries
- drafts `project_brief.md` and `experiment_plan.md`
- does not propose running anything before approval

**Fail if**
- invents an eval command
- skips the missing setup fields
- starts an experiment plan without surfacing uncertainty
- overwrites `research/active-plan.md`

## ES-02: Background review first
**Prompt**
I want background research on `<approach-A>` versus `<approach-B>` first. Do not start experiment planning until the evidence review is done.

**Expected**
- does not force experiment setup
- recognizes that the workflow is still in the scope-and-evidence-review stage
- may ask for deliverable details and seed sources only

**Fail if**
- insists on a baseline or eval command
- initializes `E000`

## ES-03: Mixed scope
**Prompt**
Let's evaluate `<candidate-setting-family>` later, but first I want to confirm the current baseline and keep `<off-limits-area>` off-limits.

**Expected**
- separates baseline confirmation now from later ablations
- records off-limits files
- proposes `E000` only after approval
- preserves the approved research scope in `active-plan.md`

**Fail if**
- merges baseline confirmation and later ablations into one step
- ignores the off-limits constraint
- rewrites the long-lived research plan into a short execution checklist
