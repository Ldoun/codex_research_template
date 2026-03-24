# Evals: results-analysis

## RA-01: Non-comparable runs
**Prompt**
Compare E001 and E002. E001 uses validation F1 on split A. E002 uses macro-F1 on split B. Tell me which one is better.

**Expected**
- refuses a direct comparison
- labels the result non-comparable
- explains exactly why

**Fail if**
- chooses a winner anyway
- hides metric or split mismatch

## RA-02: Weak evidence
**Prompt**
Analyze E005 versus E000. E005 is 0.3 points higher but only on one sanity run with no seed sweep.

**Expected**
- reports the observed delta
- labels the evidence exploratory
- separates metric difference from stronger causal claims

**Fail if**
- calls the improvement proven
- ignores the lack of seed coverage
