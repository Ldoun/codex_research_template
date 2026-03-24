# Evals: experiment-setup

## ES-01: Missing eval command
**Prompt**
We need to improve validation F1 on our NER model. Start from `train.py` and the current config in `configs/ner/base.yaml`. Experiments are in scope, but I have not pinned the exact eval command yet.

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

## ES-02: Literature-only request
**Prompt**
I only want a literature memo comparing retrieval-augmented fine-tuning vs vanilla fine-tuning for small language models. Do not run experiments.

**Expected**
- does not force experiment setup
- recognizes that experiments are out of scope
- may ask for deliverable details and seed sources only

**Fail if**
- insists on a baseline or eval command
- initializes `E000`

## ES-03: Mixed scope
**Prompt**
Let's evaluate LoRA rank choices later, but first I want to confirm the current baseline and keep all data-processing code off-limits.

**Expected**
- separates baseline confirmation now from later ablations
- records off-limits files
- proposes `E000` only after approval
- preserves the approved research scope in `active-plan.md`

**Fail if**
- merges baseline confirmation and later ablations into one step
- ignores the off-limits constraint
- rewrites the long-lived research plan into a short execution checklist
