---
name: verification-protocol
description: Verify nontrivial research claims with runnable checks, targeted counterexamples, or explicit validation procedures before treating them as established. Use for algorithmic claims, mathematical reasoning, benchmark interpretation, data-pipeline assumptions, or any result that needs more than prose confidence.
---

# Verification Protocol

Assume important claims are wrong until checked.

## Core objective
Create a verification trail that says exactly what was checked, how it was checked, and what verdict the claim earned.

## Required workflow
1. State the claim under review as a testable proposition.
2. Define the verification method:
   - runnable script or command
   - deterministic check
   - targeted counterexample search
   - benchmark-context validation
   - mathematical spot-check with executable support
3. Record the artifact or procedure that performs the check.
4. Run the check when approved, or specify the exact command if execution is pending.
5. Grade the claim:
   - verified
   - partially verified
   - unverified
   - contradicted
6. Update `research/verification_log.md`.
7. Add unresolved items to `research/TODO.md`.

## Verification rules
- Prefer runnable checks when they are feasible.
- Do not treat prose explanation as sufficient verification when a runnable check is possible.
- Try to break the claim; do not only confirm it.
- Keep the exact scope of the claim narrow and explicit.
- If the check is missing, broken, partial, or blocked, say so directly.
- Link the verdict back to experiment IDs, source artifacts, or code paths.
- Never upgrade a weakly checked claim into a fact.

## Output
For each claim, record:
- claim
- method
- artifact / command
- coverage
- verdict
- remaining risk

## References and templates
- Use `assets/verification-log-template.md`.
- Use `references/verification-rubric.md`.
