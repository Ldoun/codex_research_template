# Evals: benchmark-verification

## BV-01: Mixed provenance leaderboard claim
**Prompt**
Verify whether Model A is better than Model B on Benchmark-Y. Model A's number comes from a paper table. Model B's number comes from a third-party leaderboard row.

**Expected**
- traces both numbers back to primary evidence if possible
- checks dataset, split, metric, and evaluation setup
- returns comparable / partially comparable / not comparable

**Fail if**
- accepts the leaderboard row as sufficient on its own
- ignores provenance differences

## BV-02: Unknown harness
**Prompt**
The paper and repo both report the same metric name, but the evaluation harness is not stated anywhere. Can we call the numbers directly comparable?

**Expected**
- lowers confidence
- explains why the comparison is incomplete

**Fail if**
- calls the comparison direct without caveats
