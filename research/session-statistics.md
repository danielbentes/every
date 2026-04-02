---
title: Session Statistics
layout: default
parent: Reference
nav_order: 7
---

# Session Statistics: Every Inc AI-First Org Design Kit

## Output Summary

| Category | Files | Lines |
|---|---:|---:|
| AI-First Kit artifacts | 41 | 9,208 |
| Claude Code skills | 5 | 284 |
| CLAUDE.md | 1 | 18 |
| Research files | 3 | 2,397 |
| **Grand Total** | **50** | **11,907** |

## Artifacts by Category

| Category | Files | Lines | Description |
|---|---:|---:|---|
| Genome (identity) | 7 | 618 | Mission, values, voice, authority, tradeoffs, quality, anti-patterns |
| Governance | 7 | 1,332 | Authority matrix, boundaries, escalation, policy gen, ledger, learning loop, usage policy |
| Quality Gates | 9 | 386 | 4 gates + 4 holdout sets + index (23 holdout scenarios total) |
| Specifications | 4 | 656 | Article production, compound engineering, consulting, podcast |
| Roles | 1 | 553 | 14 roles decomposed with Three-Variable Model |
| Agents | 5 | 1,021 | 5 agent configs + index |
| Adoption | 2 | 973 | Maturity ladder (19 assessments) + 2 sprint designs |
| Evolution | 2 | 524 | Baseline audit + decision ledger |
| Operational | 2 | 2,846 | AGENT-PRIMER (175 lines) + ORG-DESIGN-DUMP (2,671 lines) |
| Coordination audit | 1 | 149 | Initial diagnostic |
| Political map | 1 | 150 | Stakeholder analysis with reframes |

## Research Phase

| Source | Articles Fetched | Insights Extracted |
|---|---:|---:|
| Chain of Thought (Dan Shipper) | 20 | 542 lines |
| Source Code (engineering) | 20 | 986 lines |
| On Every (company updates) | 23 | 869 lines |
| **Total** | **63** | **2,397 lines** |

Additional web searches: ~30 queries across multiple agents

## Agent Utilization

| Phase | Agents Spawned | Parallel? | Purpose |
|---|---:|:---:|---|
| Research wave 1 | 3 | Yes | Company research, CEO research, plugin analysis |
| Research wave 2 | 2 | Yes | Key articles, consulting/products pages |
| Research wave 3 | 3 | Yes | Chain of Thought, Source Code, On Every article batches |
| Phases 5-6 | 2 | Yes | Specifications + roles |
| Phases 7+9 | 2 | Yes | Governance + maturity ladder |
| Phases 8+10+11 | 3 | Yes | Operationalize + sprints + usage policy |
| Phases 12+13 | 2 | Yes | Agent builder + evolution auditor |
| Quality audit | 2 | Yes | Artifact consistency check + statistics |
| **Total agents** | **19** | | |

## Skills Invoked

| Skill | Phase | Invocation Method |
|---|---|---|
| coordination-audit | 1 | Direct (main agent) |
| org-genome-builder | 2 | Direct (main agent) |
| political-navigator | 3 | Direct (main agent) |
| quality-gate-designer | 4 | Direct (main agent) |
| specification-writer | 5 | Delegated to subagent |
| role-value-mapper | 6 | Delegated to subagent |
| governance-architect | 7 | Delegated to subagent |
| operationalize | 8 | Delegated to subagent (initial) + Direct (re-run) |
| maturity-ladder | 9 | Delegated to subagent |
| adoption-sprint-designer | 10 | Delegated to subagent |
| usage-policy-writer | 11 | Delegated to subagent |
| agent-builder | 12 | Delegated to subagent |
| evolution-auditor | 13 | Delegated to subagent |

## Key Metrics

- **Compression ratio:** 6,868 lines of source → 206 lines of AGENT-PRIMER (33:1) *[post-revision; original session: 9,208 → 175 = 52:1]*
- **Holdout scenarios:** 23 across 4 gates
- **Hard boundaries:** 9 non-negotiable rules
- **Team members assessed:** 19 (maturity ladder)
- **Roles mapped:** 14 (Three-Variable Model)
- **Agent configurations:** 5 (editorial, engineering, consulting, distribution, product GM) *[product GM added in revision]*
- **Claude Code skills generated:** 5 (`/org-*` commands)
- **Value conflicts modeled:** 5 specific tradeoff rules
- **Anti-patterns documented:** 10 organizational taste markers
