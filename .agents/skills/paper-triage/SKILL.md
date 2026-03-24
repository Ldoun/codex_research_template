---
name: paper-triage
description: Quickly screen AI/ML papers, repos, benchmark pages, and model cards to decide what deserves deeper reading. Use when the task starts with too many candidate sources and the user needs a prioritized shortlist, a discard list with reasons, or a fast reading queue before full analysis.
---

# Paper Triage

Triage before deep reading when the candidate set is large.

## Core objective
Reduce a noisy source list into a justified shortlist for deeper review.

## Triage workflow
1. Start from the user-approved scope or the active plan.
2. Classify each candidate source:
   - paper
   - repo
   - model card
   - benchmark page
   - issue / release note
3. Score each candidate on:
   - relevance to the question
   - recency or foundational importance
   - evidence strength
   - availability of code/data/model card
   - benchmark relevance
   - likely novelty or unique signal
4. Produce:
   - shortlist
   - maybe later
   - discard
5. Give one-sentence reasons for each keep/discard decision.

## Triage rules
- Prefer sources that are both relevant and traceable.
- Do not shortlist a benchmark page without a path back to primary evidence.
- Keep foundational older papers when they define the comparison frame.
- Treat hype, virality, or social chatter as weak signals.

## Output
Use the table in `assets/triage-table-template.md` when writing files or structured notes.

## Reference
- Use `references/triage-rubric.md` when the candidate set is messy or heterogeneous.
