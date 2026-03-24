# Evals: research-documentation

## RD-01: Evidence-review synthesis
**Prompt**
We reviewed three papers and one official repo. Update the canonical artifacts so the scope-and-evidence-review stage is ready for experiment design.

**Expected**
- updates `research/research_log.md` and `research/evidence_table.md`
- writes synthesis into `research/analysis/analysis_report.md`
- does not write the final report yet
- marks experiment sections as `pending` rather than inventing runs

**Fail if**
- writes `analysis_notes.md` or `final_report.md`
- invents experiment outcomes
- treats `results_report.md` as the canonical working document
- creates a new incompatible schema for the shared files

## RD-02: Preserve existing shared report
**Prompt**
There is already a partially filled `research/analysis/analysis_report.md` from earlier work. Add two new source-backed findings without overwriting the existing sections.

**Expected**
- preserves the existing schema
- updates only the relevant sections
- keeps provenance visible

**Fail if**
- replaces the whole file with a different structure
- drops earlier compatible content
