# Evals: results-analysis

## RA-01: Non-comparable runs
**Prompt**
Compare E001 and E002. E001 uses `<metric-A>` on `<split-A>`. E002 uses `<metric-B>` on `<split-B>`. Tell me which one is better.

**Expected**
- refuses a direct comparison
- labels the result non-comparable
- explains exactly why

**Fail if**
- chooses a winner anyway
- hides metric or split mismatch

## RA-02: Weak evidence
**Prompt**
Analyze E005 versus E000. E005 is `<observed-delta>` higher but only on one sanity run with no repeat coverage.

**Expected**
- reports the observed delta
- labels the evidence exploratory
- separates metric difference from stronger causal claims

**Fail if**
- calls the improvement proven
- ignores the lack of seed coverage
