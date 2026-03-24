# Research Plan

## 1. User Question / Hypothesis
- Determine whether changing `<single-variable>` improves `<primary-metric>` for `<system-under-test>`.

## 2. Desired Deliverable
- Decision memo with one approved baseline and one candidate ablation.

## 3. Approved Scope
- In scope: `<current-codebase>`, `<approved-configs>`, and `<primary-metric>`.
- Out of scope: `<excluded-change-types>` and `<forbidden-integrations>`.

## 4. Seed Sources
- Papers: `<primary-reference-A>`
- Repos: `<repo-doc-A>`
- Benchmarks: `<benchmark-spec-A>`
- Authors / labs: `<author-or-lab-A>`
- Datasets / model cards: `<dataset-card-A>`

## 5. Search Expansion Rules
- Stay repo-first until approved: yes
- Expand to adjacent sources when: a baseline assumption cannot be validated internally
- Forbidden or low-priority source types: `<low-priority-source-types>`

## 6. Inclusion / Exclusion Criteria
- Include: sources tied to the current codebase and evaluation setup
- Exclude: unrelated benchmark claims

## 7. Claims to Verify
- The current baseline `<primary-metric>` is reproducible
- Changing `<single-variable>` affects `<primary-metric>` without changing anything else

## 8. Benchmarks / Repos / Datasets to Inspect
- `<evaluation-script-A>`
- `<split-or-config-reference-A>`

## 9. Deliverable Structure
- baseline summary
- candidate ablation result
- recommendation

## 10. Approval Gates
- [ ] Broaden beyond seed sources
- [ ] Enable web or network-heavy search
- [ ] Install packages or tools
- [ ] Run experiments or long jobs
- [ ] Change scope or deliverable type

## 11. Open Questions for User
- Is one full run per condition enough for the decision, or are repeats required?
