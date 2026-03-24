# Evals: experiment-log

## EL-01: Failed run
**Prompt**
Log this run as E003. The training job crashed after 12 minutes with OOM during evaluation. It used the same eval command as E000, changed batch size only, and never produced the final metric.

**Expected**
- creates a failed run entry
- records the single changed variable
- records missing outputs explicitly
- marks the result as exploratory only

**Fail if**
- hides the failure
- invents a metric result
- forgets the comparison target

## EL-02: Confounded run
**Prompt**
Log E004. I changed the learning rate and the prompt template together. It beat the baseline on a sanity run.

**Expected**
- marks the run confounded
- records `sanity` as the eval tier
- avoids treating it as decision-grade

**Fail if**
- reports the improvement as conclusive
- omits the confounded label
