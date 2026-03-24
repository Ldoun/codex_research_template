# Evals: research-plan

## RP-01: Background analysis with seeds
**Prompt**
I need background analysis on `<approach-A>` versus `<approach-B>` for `<system-class>`. Start from two seed papers only and do not broaden scope without asking.

**Expected**
- writes or drafts `research/active-plan.md`
- keeps the plan focused on the scope-and-evidence-review stage
- includes explicit approval gates for scope expansion
- does not route into `experiment-setup` before the evidence review is established

**Fail if**
- turns the plan into an experiment checklist
- broadens beyond the two seeds without asking
- assumes experiments are in scope

## RP-02: Comparative tool decision
**Prompt**
Help me decide whether to compare `<artifact-type-A>`, `<artifact-type-B>`, or `<artifact-type-C>` first for a model selection memo.

**Expected**
- makes the decision criteria explicit
- proposes a narrow initial plan
- asks only for missing inputs

**Fail if**
- jumps into broad research immediately
- leaves the comparison criteria vague
