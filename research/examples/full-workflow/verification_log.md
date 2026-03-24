# Verification Log

| Claim ID | Claim | Method | Artifact / command | Coverage | Verdict | Linked experiment(s) | Notes |
|---|---|---|---|---|---|---|---|
| C001 | E000 used the approved evaluation command and baseline setting | direct command and config inspection | `<evaluation-script-A>`, `<config-path-A>`, `<run-output-A>` | full | verified | E000 | baseline context matches the brief |

## Detailed entries

### C001
- Claim: E000 matches the approved baseline context.
- Why it matters: later ablations are not interpretable if the baseline drifts.
- Verification method: inspect command, config, and output artifact.
- Artifact / command: `<exact-eval-command>`
- What passed: command, split, and baseline setting matched the brief.
- What failed: nothing.
- Scope limits: does not yet verify future runs.
- Final verdict: verified
- Next action: request approval for E001 candidate ablation.
