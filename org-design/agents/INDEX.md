---
title: Agents
layout: default
nav_order: 8
has_children: true
---

# Agent Registry — Every Inc
<!-- Updated: 2026-04-02-0130 -->

## Agent Registry

| Agent | Directory | Role | Authority Scope | Applicable Gates | Human Owner |
|-------|-----------|------|-----------------|------------------|-------------|
| [Editorial Quality]({% link org-design/agents/editorial-quality/index.md %}) | `editorial-quality/` | Reviews articles against three rigor tests + AI tells detection | Tier 1 (analysis), Tier 2 (detection), Tier 3 (publication) | [article-publication]({% link org-design/gates/article-publication.md %}) | Kate Lee + Katie Parrott |
| [Compound Engineering]({% link org-design/agents/compound-engineering/index.md %}) | `compound-engineering/` | Executes Plan→Work→Review→Compound cycle | Tier 1 (code gen/review), Tier 2 (auto-fix/compound), Tier 3 (merge) | [code-merge]({% link org-design/gates/code-merge.md %}) | Product GM (Kieran/Naveen/Yash/Danny) |
| [Consulting PM (Claudie)]({% link org-design/agents/consulting-pm/index.md %}) | `consulting-pm/` | Manages consulting engagement logistics, status, deliverables | Tier 1 (internal), Tier 2 (status/prep), Tier 3 (deliverables) | [consulting-deliverable]({% link org-design/gates/consulting-deliverable.md %}) | Natalia Quintero |
| [Content Distribution]({% link org-design/agents/content-distribution/index.md %}) | `content-distribution/` | Generates social posts from published articles | Tier 1 (draft gen), Tier 2 (queue), Tier 3 (posting) | [social-media-publication]({% link org-design/gates/social-media-publication.md %}) | Anthony Scarpulla |
| [Product GM]({% link org-design/agents/product-gm/index.md %}) | `product-gm/` | Full-stack specification authority: PRDs, compound engineering cycle, merge decisions | Tier 1 (code gen/review/triage), Tier 2 (auto-fix/compound), Tier 3 (merge) | [code-merge]({% link org-design/gates/code-merge.md %}) | Product GM (Kieran/Naveen/Yash/Danny) |

## Directory Structure Per Agent

Each agent directory contains:
```
agents/{role-slug}/
  system-prompt.md        — Core: identity, context, boundaries, capabilities, collaboration, prompt, reporting
  tool-permissions.md     — Action/Permission/Condition table
  self-review-checklist.md — Gate-derived checklist with checkbox items
```

## Authority Tier Summary

| Tier | Editorial Quality | Compound Engineering | Consulting PM (Claudie) | Content Distribution | Product GM |
|------|------------------|---------------------|------------------------|---------------------|------------|
| **Tier 1** (Autonomous) | Structural analysis, text scanning | Code gen, test execution, 14-agent review | Internal tracking, research, milestone monitoring | Article extraction, voice profiling, draft generation | PRD/plan writing, code gen, review pipeline, bug triage, research |
| **Tier 2** (Autonomous + Notify) | AI tells detection, rigor test evaluation | Bug auto-fix, CLAUDE.md updates, knowledge base entries | Status report generation, onboarding workflows, training prep | Draft queuing for Anthony's review | P1 auto-fix, compound artifacts, knowledge base updates, design requests |
| **Tier 3** (Human-in-Loop) | Publication recommendation (Kate, 48h) | Code merge (GM, 24h) | Deliverable delivery (Natalia, 24h), client comms | Social posting (Author + Anthony, 12h) | Code merge (GM, 24h), cross-product data, shared infra |
| **Tier 4** (Never) | Editorial direction | Architecture decisions, other GM's config | Financial commitments, cross-engagement data | Social strategy | Architecture decisions, pricing, other GM's config |

## Hard Boundary Coverage

| Boundary | Editorial Quality | Compound Engineering | Consulting PM | Content Distribution | Product GM |
|----------|:---:|:---:|:---:|:---:|:---:|
| 1. Never publish without review | Primary | -- | -- | Primary | Relevant |
| 2. Never send external comms | -- | -- | Primary | Primary | Relevant |
| 3. Never make financial commitments | -- | -- | Primary | -- | Relevant |
| 4. Never share client data cross-engagement | -- | -- | Primary | -- | -- |
| 5. Never merge without review gate | -- | Primary | -- | -- | Primary |
| 6. Never change another GM's config | -- | Primary | -- | -- | Primary |
| 7. Never exceed product PII scope | -- | Primary | -- | -- | Primary |
| 8. Never make ungrounded claims | Primary | -- | Primary | Primary | Relevant |
| 9. Never bypass quality gates | Primary | Primary | Primary | Primary | Primary |

## Future Agent Candidates

Based on the coordination audit's encoding candidates:

| Candidate | Domain | Est. Hours Saved/Month | Coordination Audit Reference |
|-----------|--------|:---:|---|
| Design Request Intake Agent | Design team | ~32 | Quick Win #1: formalize design intake in Linear |
| Editorial Pipeline Agent | Editorial | ~17 | Quick Win #3: automated Kanban nudges |
| Cross-GM Knowledge Feed Agent | Engineering | ~12 | Quick Win #3: shared learnings from compound loops |
| Podcast Logistics Agent | Podcast | ~12 | Encoding candidate #5 |
