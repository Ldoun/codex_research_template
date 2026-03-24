# Research Plan

## 1. User Question / Hypothesis
- Compare `<approach-A>` versus `<approach-B>` for `<task-or-system-class>` under `<constraint-set>`.

## 2. Desired Deliverable
- Background analysis memo with a recommendation for whether experiments are justified.

## 3. Approved Scope
- In scope: `<approved-source-types>` tied to `<system-boundary>`.
- Out of scope: `<excluded-source-types>` and `<out-of-scope-claims>`.

## 4. Seed Sources
- Papers: `<seed-paper-A>`, `<seed-paper-B>`
- Repos: `<official-repo-A>`
- Benchmarks: `<benchmark-doc-A>`
- Authors / labs: `<author-or-lab-A>`
- Datasets / model cards: `<dataset-or-model-card-A>`

## 5. Search Expansion Rules
- Stay seed-first until approved: yes
- Expand to adjacent sources when: a benchmark or implementation claim cannot be verified from seeds
- Forbidden or low-priority source types: `<low-priority-source-types>`

## 6. Inclusion / Exclusion Criteria
- Include: traceable sources with concrete setup details
- Exclude: claims without dataset, split, or metric context

## 7. Claims to Verify
- Whether `<approach-A>` consistently helps relative to `<approach-B>` on the approved scope
- Whether the reported gains depend on `<setup-factor>`

## 8. Benchmarks / Repos / Datasets to Inspect
- `<benchmark-or-dataset-A>`
- `<evaluation-harness-A>`

## 9. Deliverable Structure
- recommendation
- evidence-backed comparison
- open questions

## 10. Approval Gates
- [ ] Broaden beyond seed sources
- [ ] Enable web or network-heavy search
- [ ] Install packages or tools
- [ ] Run experiments or long jobs
- [ ] Change scope or deliverable type

## 11. Open Questions for User
- Are third-party summaries acceptable if they link back to primary evidence?
