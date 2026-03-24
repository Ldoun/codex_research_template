---
name: benchmark-verification
description: Verify AI/ML benchmark claims against papers, official repos, model cards, evaluation scripts, and benchmark documentation. Use when benchmark tables, leaderboard positions, or "SOTA" claims affect the recommendation and need apples-to-apples verification.
---

# Benchmark Verification

Benchmark claims are only useful when their context is verified.

## Core objective
Decide whether a benchmark claim is directly comparable, partially comparable, or not comparable.

## Verification workflow
1. Identify the exact claim to verify.
2. Trace the claim back to the highest-quality available source.
3. Capture the comparison context:
   - model and version
   - dataset and split
   - metric
   - evaluation harness / script
   - prompting or few-shot setup
   - filtering or post-processing
   - hardware / runtime context when relevant
   - date / release / commit context
4. Compare candidates only after the contexts are aligned.
5. Return a verdict:
   - comparable
   - partially comparable
   - not comparable
6. If the benchmark interpretation itself is a critical claim, hand off to `verification-protocol` for a fuller verification trail.

## Required cautions
- Do not treat third-party leaderboard rows as sufficient by themselves.
- Do not merge paper numbers and repo numbers without noting the difference.
- Do not call something "SOTA" without the benchmark scope and date context.
- If the metric or split differs, say the comparison is not direct.
- If the evaluation harness is unknown, lower confidence.

## Output format
Use this order:
- Claim under review
- Primary source(s)
- Verified setup details
- Comparability verdict
- Important caveats
- Recommended next check, if any

## References and templates
- Use `references/verification-checklist.md`.
- Use `assets/verification-notes-template.md` for persistent notes.
