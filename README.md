# Every Inc: Organizational Genome

This repository contains the complete output of running the [AI-First Org Design Kit](https://github.com/synaptiai/synapti-marketplace/tree/main/plugins/ai-first-org-design-kit) on Every Inc, a ~20-person media-software-consulting company that writes about AI, builds AI tools, and teaches companies to adopt AI.

**[Browse the full output of the experiement →](https://danielbentes.github.io/every/)**

**Article:** [Your Agents Don't Know Who You Are](article.md)

## The Experiment

One Claude Code session, acting as Every's CEO Dan Shipper, ran the complete 14-skill AI-First Org Design Kit end-to-end, from coordination audit to evolution auditor, producing a full organizational genome, governance framework, quality gates, workflow specifications, role definitions, agent configurations, adoption infrastructure, and evolution mechanisms.

No human intervention between phases. The agent answered all interview questions itself, drawing on research from 63 Every newsletters and articles.

The article itself is part of the experiment: written as Dan Shipper, in his voice, about the process of encoding Every's organizational operating system — produced by the same session that generated the artifacts it describes.

*The experiment was run on public information from Every's published articles. Dan Shipper and the Every team were not involved in producing this output --- it's a demonstration of what the kit can do with publicly available organizational signal. That said: Dan, Kate, Natalia, Kieran, Danny, Naveen, Yash --- if you're reading this, I hope the output does justice to what you've built. Every is one of the most legible AI-first organizations out there, which is exactly why it made for such a compelling test case.*

## By the Numbers


| Metric                           | Value                             |
| -------------------------------- | --------------------------------- |
| Total files produced             | 75                                |
| Articles researched              | 63                                |
| Skills invoked                   | 14 (full kit)                     |
| Genome files                     | 7                                 |
| Governance documents             | 7                                 |
| Quality gates                    | 4 (with 23 holdout scenarios)     |
| Workflow specifications          | 4                                 |
| Roles mapped                     | 14                                |
| Agent configurations             | 5 (with 4 framework exports each) |
| Claude Code sub-agents           | 5                                 |
| Claude Code governance skills    | 5                                 |
| Hard boundaries defined          | 9                                 |
| Anti-patterns documented         | 10                                |
| Team members assessed (maturity) | 19                                |
| AGENT-PRIMER compression ratio   | 33:1                              |


## Browsing the Specification

The complete organizational specification created for Every is published as a searchable documentation site:

**[danielbentes.github.io/every →](https://danielbentes.github.io/every/)**

The site has sidebar navigation, full-text search, and breadcrumbs. Here's what you'll find:


| Section                              | What It Contains                                                                                 |
| ------------------------------------ | ------------------------------------------------------------------------------------------------ |
| [Genome](org-design/genome/)         | Who Every is — mission, values as decision rules, voice norms, quality standards, anti-patterns  |
| [Governance](org-design/governance/) | How agents operate — authority tiers, 9 hard boundaries, escalation protocols, policy generation |
| [Quality Gates](org-design/gates/)   | 4 gates with pass/fail criteria and 23 hidden holdout test scenarios                             |
| [Specifications](org-design/specs/)  | Workflow specs for articles, engineering, consulting, podcasts — pass the Stranger Test          |
| [Agents](org-design/agents/)         | 5 agent configs with system prompts, tool permissions, and self-review checklists                |
| [Adoption](org-design/adoption/)     | Maturity ladder (19 people assessed) and sprint designs for AI adoption                          |
| [Evolution](org-design/evolution/)   | Decision ledger and monthly governance review cycle                                              |
| [Reference](research/)               | 63-article research extracts, session narrative, style guide, statistics                         |


Additional infrastructure in the repo (not on the docs site):

- `**CLAUDE.md`** — Uses `@imports` to auto-load mission, values, and hard boundaries into every Claude Code session
- `**.claude/agents/**` — 5 sub-agent registrations invokable via `@agent-name`
- `**.claude/skills/**` — 5 governance skills: `/org-voice-check`, `/org-gate-review`, `/org-record-decision`, `/org-values-check`, `/org-novel-situation`
- `**org-design/AGENT-PRIMER.md**` — 206-line compressed primer any agent can load at session start (33:1 compression)
- **Framework exports** — Each agent has configs for Anthropic Agent SDK, OpenAI Agents SDK, CrewAI, and OpenClaw

## What the Kit Produced

### Layer 1: Identity (The Genome)

Who Every is, encoded as decision rules. Five values with Builder Credibility as the absolute tiebreaker that is never compromised. Voice norms that say "use 'taste' and 'ship'" and "never say 'leverage' or 'synergy.'" Quality standards per output type. Ten anti-patterns that define what "not us" looks like.

### Layer 2: Operations (Governance + Gates)

How agents operate within Every's boundaries. Nine hard boundaries (never publish without human review, never share client data cross-engagement, never bypass quality gates). Four quality gates with 23 hidden holdout scenarios for validation. Escalation protocols with 2-minute decision format. A policy generation mechanism so governance grows from evidence, not committee meetings.

### Layer 3: Roles + Workflows (Specifications)

How work flows through Every. Four workflow specifications that pass the Stranger Test. Fourteen roles decomposed into specification/coordination/execution time allocation. The Two-Slice Team model formalized: each GM runs their product solo with 99% AI-written code.

### Layer 4: Agents + Evolution (Deployment)

How to deploy and evolve. Five agent configurations (editorial, engineering, consulting, distribution, product GM) with system prompts, tool permissions, self-review checklists, and framework exports for Anthropic Agent SDK, OpenAI Agents SDK, CrewAI, and OpenClaw. Maturity ladder assessing 19 team members. Two adoption sprint designs. A decision ledger and monthly evolution audit cycle.

### Layer 5: Operationalization (The Bridge)

AGENT-PRIMER.md distills ~7,000 lines of specification into 206 actionable operating rules any agent can load (33:1 compression). CLAUDE.md with @imports so governance auto-loads at session start. Five invokable `/org-`* skills for governance operations. Five Claude Code sub-agents registered for direct invocation via `@agent-name`.

## Key Insight

The hardest part of AI-first org design is not the framework. It's the excavation. Articulating implicit organizational knowledge ("what does 'taste' actually mean when you have to encode it for an agent?") is a genuinely difficult intellectual exercise. The 63-article research phase was the investment that made everything downstream credible.

## How It Was Made

One Claude Code session ran the complete 14-skill AI-First Org Design Kit, acting as Every's CEO based on research into 63 published articles. The session produced all artifacts without human intervention between phases, then underwent two revision passes for quality and structural conformance.

## The Plugin

The AI-First Org Design Kit is available on the [Synapti Marketplace](https://github.com/synaptiai/synapti-marketplace): [ai-first-org-design-kit](https://github.com/synaptiai/synapti-marketplace/tree/main/plugins/ai-first-org-design-kit)

Install via the [Synapti Marketplace](https://github.com/synaptiai/synapti-marketplace) in Claude Code.

### Add the Synapti marketplace

`/plugin marketplace add synaptiai/synapti-marketplace`

### Install the kit

`/plugin install ai-first-org-design-kit@synapti-marketplace`

Then run `/ai-first-kit` to start. Set aside enough time and bring your favorite beverage!

## The Conceptual Foundation

[The Specification Economy](https://medium.com/@danielbentes/the-specification-economy-77f7d2297c37)