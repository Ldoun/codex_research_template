# Research Plan

## 1. Research Question / Decision
- Determine whether changing LoRA rank improves validation F1 for the current NER system.

## 2. Desired Deliverable
- Decision memo with one approved baseline and one candidate ablation.

## 3. Approved Scope
- In scope: current training pipeline, official repo docs, existing configs, validation F1
- Out of scope: dataset relabeling, architecture changes, and third-party APIs

## 4. Seed Sources
- Papers: original LoRA paper
- Repos: internal NER repo, official LoRA docs
- Benchmarks: internal validation split notes
- Authors / labs: N/A
- Datasets / model cards: internal NER dataset card

## 5. Search Expansion Rules
- Stay repo-first until approved: yes
- Expand to adjacent sources when: a baseline assumption cannot be validated internally
- Forbidden or low-priority source types: social chatter and unsourced blog comparisons

## 6. Inclusion / Exclusion Criteria
- Include: sources tied to the current codebase and evaluation setup
- Exclude: unrelated benchmark claims

## 7. Claims to Verify
- Current baseline F1 is reproducible
- Increasing LoRA rank changes F1 without changing anything else

## 8. Benchmarks / Repos / Datasets to Inspect
- internal `eval.py`
- validation split config

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
- Is one full validation run enough for the decision, or is a seed sweep required?
