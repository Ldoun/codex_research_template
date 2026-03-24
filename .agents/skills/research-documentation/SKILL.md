---
name: research-documentation
description: Maintain structured, auditable research documentation with logs, evidence tables, canonical analysis reports, and canonical final reports. Use when gathering findings, drafting literature reviews or comparison memos, keeping claim-to-source traceability, or turning scattered notes into a clear report with uncertainty labels.
---

# Research Documentation

Keep the research traceable. Documentation is not optional once evidence starts accumulating.

## Core objective
Convert raw findings into durable artifacts that preserve provenance, uncertainty, and decision context.

## Canonical artifacts
Use or update these files under `research/` as needed:
- `active-plan.md`
- `research_log.md`
- `evidence_table.md`
- `analysis/analysis_report.md`
- `results_report.md`

Initialize them from the templates in `assets/` when they do not exist.

For experiment-specific artifacts, use:
- `experiment-log` for run records
- `results-analysis` for experiment comparison sections in the shared analysis report
- `verification-protocol` for claim verification logs

## Documentation workflow
1. Log each meaningful research action in `research_log.md`:
   - date
   - query or source reviewed
   - keep / discard decision
   - brief reason
   - next step
2. Add evidence rows to `evidence_table.md` for every claim that matters.
3. Keep interpretation and synthesis in `analysis/analysis_report.md`, using the canonical shared schema.
4. Draft or update `results_report.md` only from evidence that is already logged.
5. If shared artifacts already exist, update the relevant sections instead of replacing them with a new schema.
6. End every update with:
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
- prompting, few-shot, or system setup, if relevant
- hardware or runtime context, if relevant
- whether the source is the paper, official repo, model card, or a third party

## Writing rules
- Separate fact from interpretation.
- Mark open questions explicitly.
- Preserve conflicting evidence instead of overwriting it.
- Do not silently delete superseded reasoning; mark it as revised.
- Prefer concise, source-backed sentences over long unsupported prose.
- For literature-only work, mark experiment sections as `N/A` rather than inventing experiment content.

## References and templates
- Use `assets/research-log-template.md`.
- Use `assets/evidence-table-template.md`.
- Use `assets/analysis-report-template.md`.
- Use `assets/results-report-template.md`.
- Use `references/source-hierarchy.md` when deciding source quality.
