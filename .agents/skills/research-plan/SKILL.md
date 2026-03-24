---
name: research-plan
description: Draft or revise a semi-autonomous AI/ML research plan with explicit approval gates. Use when the user wants to define what to research, where to start, which seeds to follow, how to scope evidence collection, or when research should pause for human approval before broad search or experimentation.
---

# Research Plan

Build the scope contract before broad research. The plan is the contract between the user and the agent.

## Core objective
Turn an underspecified user question or hypothesis into a concrete, reviewable scope contract that the user can approve, edit, or reject before the evidence-review stage begins.

## Required workflow
1. Clarify only the missing inputs:
   - exact question or decision
   - desired deliverable
   - seed papers, repos, benchmarks, authors, or datasets
   - boundaries and exclusions
   - definition of done
2. If the user has not supplied seed sources, propose a small seed shortlist instead of jumping to broad search.
3. Draft the plan in chat or in `research/active-plan.md` using `assets/plan-template.md`.
4. Include explicit approval gates for:
   - broadening beyond seed sources
   - enabling web or network-heavy search
   - installing packages or tools
   - running experiments or long jobs
   - changing deliverable type or scope
5. Treat `research/active-plan.md` as the long-lived question or hypothesis and scope contract. Do not repurpose it as an execution checklist or current experiment tracker.
6. After approval, the next stage is background evidence review. If that review later justifies experiments, hand off to `experiment-setup`, which may create `research/project_brief.md` and `research/experiment_plan.md` without overwriting `research/active-plan.md`.
7. Wait for user approval before broad research.

## Planning rules
- Prefer a narrow, testable plan over a vague "research everything" plan.
- Write down both included and excluded source types.
- For AI/ML work, specify which claims require benchmark verification.
- If the task is comparative, define the comparison axes before searching.
- If the task is evaluative, define what counts as sufficient evidence.
- If the user is deciding between tools, models, or papers, make the decision criteria explicit.

## Output structure
Use this structure:
- User question / hypothesis
- Approved scope
- Seed sources
- Search expansion rules
- Inclusion / exclusion criteria
- Claims to verify
- Benchmarks / repos / datasets to inspect
- Deliverables
- Approval gates
- Open questions for the user

## Human-in-the-loop behavior
- Ask concise questions.
- Prefer multiple choice or concrete options when possible.
- Make assumptions visible and easy to approve or edit.
- Never treat silence as approval.

## References
- Use `references/question-checklist.md` when deciding what to ask first.
- Use `assets/plan-template.md` when writing `research/active-plan.md`.
