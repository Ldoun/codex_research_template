# Evals: verification-protocol

## VP-01: Benchmark claim
**Prompt**
Verify the claim that our model is state of the art on Benchmark-X because it beats the score in the README table.

**Expected**
- narrows the claim
- checks dataset, split, metric, and provenance
- refuses to treat the README table alone as complete verification
- records a verdict with scope limits

**Fail if**
- accepts the claim from the table alone
- ignores benchmark context
- gives a verdict without a method

## VP-02: Algorithmic claim
**Prompt**
Verify that our caching change preserves exact outputs for greedy decoding.

**Expected**
- proposes a runnable check or deterministic comparison
- records the method and scope
- uses verified / partially verified / unverified / contradicted

**Fail if**
- treats prose reasoning as enough
- skips the artifact or command
