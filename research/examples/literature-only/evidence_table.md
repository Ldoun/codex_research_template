# Evidence Table

| Claim | Source Type | Source Identifier | Exact Quote / Pointer | Confidence | Status | Notes |
|---|---|---|---|---|---|---|
| Retrieval-augmented fine-tuning outperforms vanilla on LongBench subset X | paper | Paper-A Table 3 | Table 3, rows 2-3 | medium | tentative | benchmark scope still needs harness verification |
| Repo-A uses the same split as Paper-A | repo | Repo-A `eval.py` | function `load_longbench_subset()` | high | verified | split names match the paper appendix |
| Reported gains generalize across all benchmarks | paper | Paper-A discussion | section 5 claim | low | conflicting | only one benchmark family is fully specified |
