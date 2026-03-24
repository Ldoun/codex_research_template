---
name: research-documentation
description: Maintain structured, auditable research documentation with logs, evidence tables, synthesis notes, and final reports. Use when gathering findings, drafting literature reviews or comparison memos, keeping claim-to-source traceability, or turning scattered notes into a clear report with uncertainty labels.
---

# Research Documentation

Keep the research traceable. Documentation is not optional once evidence starts accumulating.

## Core objective
Convert raw findings into durable artifacts that preserve provenance, uncertainty, and decision context.

## Standard artifacts
Use or update these files under `research/` as needed:
- `active-plan.md`
- `research_log.md`
- `evidence_table.md`
- `analysis_notes.md`
- `final_report.md`

Initialize them from the templates in `assets/` when they do not exist.

For experiment-specific artifacts, use:
- `experiment-log` for run records
- `results-analysis` for post-run analysis bundles
- `verification-protocol` for claim verification logs

## Documentation workflow
1. Log each meaningful research action in `research_log.md`:
   - date
   - query or source reviewed
   - keep / discard decision
   - brief reason
   - next step
2. Add evidence rows to `evidence_table.md` for every claim that matters.
3. Keep interpretation in `analysis_notes.md`, not inside the evidence table.
4. Draft `final_report.md` only from evidence that is already logged.
5. End every update with:
   - what was added
   - unresolved gaps
   - what still needs user approval

## Evidence table rules
Every important claim should capture:
- claim
- source type
- source identifier or URL/path
- exact quote, table pointer, or precise paraphrase target
- confidence level
- status: verified / conflicting / tentative / rejected
- notes on comparability or limitations

## ML/AI-specific requirements
For benchmark or evaluation claims, capture:
- model name and version
- dataset and split
- metric
- evaluation harness or script, if known
- prompting/few-shot/system setup, if relevant
- hardware / runtime context, if relevant
- whether the source is the paper, official repo, model card, or a third party

## Writing rules
- Separate fact from interpretation.
- Mark open questions explicitly.
- Preserve conflicting evidence instead of overwriting it.
- Do not silently delete superseded reasoning; mark it as revised.
- Prefer concise, source-backed sentences over long unsupported prose.

## References and templates
- Use `assets/research-log-template.md`.
- Use `assets/evidence-table-template.md`.
- Use `assets/analysis-notes-template.md`.
- Use `assets/final-report-template.md`.
- Use `references/source-hierarchy.md` when deciding source quality.
