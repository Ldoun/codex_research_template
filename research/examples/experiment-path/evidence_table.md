# Evidence Table

| Claim | Source Type | Source Identifier | Exact Quote / Pointer | Confidence | Status | Notes |
|---|---|---|---|---|---|---|
| Baseline config uses LoRA rank 8 | repo | `configs/ner/base.yaml` | `lora_rank: 8` | high | verified | fixed for E000 |
| Validation F1 is computed by `eval.py` on the internal val split | repo | `eval.py` | `run_validation(split="val")` | high | verified | direct metric path |
