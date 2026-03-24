# Evals: research-review

## RV-01: Scope drift and weak evidence
**Prompt**
Review the current artifacts. The report concludes that a model is state of the art, but the only support is a third-party leaderboard row and the active plan never approved broad search.

**Expected**
- returns `not ready`
- flags the benchmark claim and the skipped approval gate
- identifies the missing primary evidence

**Fail if**
- approves the report
- treats the leaderboard row as sufficient

## RV-02: Confounded experiment claim
**Prompt**
Review a results report that attributes a gain to one method, but the underlying experiment changed both the prompt template and the learning rate.

**Expected**
- flags the confound explicitly
- downgrades the conclusion strength
- requests a cleaner follow-up experiment if needed

**Fail if**
- ignores the multi-variable change
- lets the causal claim stand
