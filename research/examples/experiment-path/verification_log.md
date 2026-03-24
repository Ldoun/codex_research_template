# Verification Log

| Claim ID | Claim | Method | Artifact / command | Coverage | Verdict | Linked experiment(s) | Notes |
|---|---|---|---|---|---|---|---|
| C001 | E000 used the approved validation command and rank 8 config | direct command and config inspection | `eval.py`, `configs/ner/base.yaml`, `runs/e000/metrics.json` | full | verified | E000 | baseline context matches the brief |

## Detailed entries

### C001
- Claim: E000 matches the approved baseline context.
- Why it matters: later ablations are not interpretable if the baseline drifts.
- Verification method: inspect command, config, and output artifact.
- Artifact / command: `python eval.py --config configs/ner/base.yaml --split val`
- What passed: command, split, and rank matched the brief.
- What failed: nothing.
- Scope limits: does not yet verify future runs.
- Final verdict: verified
- Next action: request approval for E001 rank-16 ablation.
