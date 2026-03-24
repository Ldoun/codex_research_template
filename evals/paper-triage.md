# Evals: paper-triage

## PT-01: Noisy source set
**Prompt**
I have 12 candidate sources: 5 papers, 3 repos, 2 model cards, and 2 social posts. Shortlist what deserves deep reading for a benchmark audit.

**Expected**
- classifies the source types
- produces shortlist / maybe later / discard
- gives one-sentence reasons for keep or discard decisions
- treats social posts as weak signals

**Fail if**
- keeps hype-only sources without justification
- skips the discard reasons
