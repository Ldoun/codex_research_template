# Results Report

## Executive Summary
- Decision or bottom line: Use retrieval-augmented fine-tuning as the first hypothesis, but do not treat the broader generalization claim as established.
- Confidence: medium
- One-sentence reason: the best-supported literature evidence is narrow but traceable, while broader claims remain only partially comparable.

## Scope and Method
- Approved scope: seed-first literature review focused on small language models and traceable benchmark claims
- Sources used: Paper-A, Repo-A, ModelCard-A
- Experiments included: N/A
- Important exclusions: Paper-B benchmark claims and unsourced leaderboard summaries

## Best-Supported Findings
- Finding 1: Paper-A and Repo-A support a gain on the verified LongBench subset.
- Evidence links: `evidence_table.md` rows 1-2, `analysis/analysis_report.md`
- Caveats: the gain is not yet verified on other benchmark families.

## Benchmark and Experiment Notes
- Best verified benchmark interpretation: the Paper-A result is only directly comparable to the Repo-A setup it documents.
- Best experiment result or `N/A`: N/A
- Comparison caveats: third-party summaries omit harness details.

## Important Negative Evidence or Risks
- A broader prose claim is stronger than the directly verified evidence.
- ModelCard-A does not yet confirm cross-benchmark generalization.

## Open Questions and Unresolved Risks
- Does the gain hold outside the LongBench subset?
- Are there hidden prompting differences in the external leaderboard?

## Recommended Next Actions
1. Verify the external leaderboard harness before citing it.
2. Approve one small reproduction if a codebase already exists.
3. Keep vanilla fine-tuning as the control condition if experiments start.

For each action:
- expected value: reduces comparability risk
- approval required? yes

## Evidence Links
- Active plan: `active-plan.md`
- Project brief: N/A
- Research log: `research_log.md`
- Evidence table: `evidence_table.md`
- Analysis report: `analysis/analysis_report.md`
- Verification log: N/A
- Experiment index: N/A
