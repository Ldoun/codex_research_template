# Research Plan

## 1. Research Question / Decision
- Compare retrieval-augmented fine-tuning versus vanilla fine-tuning for small language models under limited compute.

## 2. Desired Deliverable
- Literature memo with a recommendation for whether experiments are worth running later.

## 3. Approved Scope
- In scope: papers, official repos, model cards, and benchmark docs tied to <13B models.
- Out of scope: closed-source-only systems and social-post-only claims.

## 4. Seed Sources
- Papers: Paper-A, Paper-B
- Repos: Repo-A
- Benchmarks: LongBench subset notes
- Authors / labs: Lab-A
- Datasets / model cards: ModelCard-A

## 5. Search Expansion Rules
- Stay seed-first until approved: yes
- Expand to adjacent sources when: a benchmark or implementation claim cannot be verified from seeds
- Forbidden or low-priority source types: unsourced leaderboards and social posts

## 6. Inclusion / Exclusion Criteria
- Include: traceable sources with concrete setup details
- Exclude: claims without dataset, split, or metric context

## 7. Claims to Verify
- Whether retrieval-augmented fine-tuning consistently helps under low compute
- Whether the reported gains depend on benchmark or prompting setup

## 8. Benchmarks / Repos / Datasets to Inspect
- LongBench subset used in Paper-A
- Repo-A evaluation harness

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
- Are third-party benchmark dashboards acceptable if they link to primary evidence?
