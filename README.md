# Every Inc: Organizational Genome

This repository contains the complete output of running the [AI-First Org Design Kit](https://github.com/synaptiai/synapti-marketplace/tree/main/plugins/ai-first-org-design-kit) on Every Inc, a ~20-person media-software-consulting company that writes about AI, builds AI tools, and teaches companies to adopt AI.

**Article:** [Your Agents Don't Know Who You Are](article.md)

## The Experiment

One Claude Code session, acting as Every's CEO Dan Shipper, ran the complete 14-skill AI-First Org Design Kit end-to-end, from coordination audit to evolution auditor, producing a full organizational genome, governance framework, quality gates, workflow specifications, role definitions, agent configurations, adoption infrastructure, and evolution mechanisms.

No human intervention between phases. The agent answered all interview questions itself, drawing on research from 63 Every newsletters and articles.

The article itself is part of the experiment: written as Dan Shipper, in his voice, about the process of encoding Every's organizational operating system — produced by the same session that generated the artifacts it describes.

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


## What's Here

### `org-design/` — The Complete Organizational Specification

75 files across identity, governance, quality gates, workflows, agents, adoption, and evolution:

```
org-design/
├── AGENT-PRIMER.md                          # Distilled operating guide for agents (33:1 compression)
├── ORG-DESIGN-DUMP-2026-04-02-0120.md       # Full artifact dump (point-in-time snapshot)
├── audit-2026-04-01-1427.md                 # Coordination audit (where human time goes)
├── political-map-2026-04-01-1436.md         # Stakeholder analysis and change sequencing
├── roles-2026-04-01-1440.md                 # 14 roles mapped with Three-Variable Model
│
├── genome/                                   # Who we are (identity layer)
│   ├── 00-identity/
│   │   ├── MISSION.md                       # Operational mission + exclusions
│   │   ├── VALUES.md                        # 5 values as decision rules with conflict resolution
│   │   └── VOICE.md                         # Communication norms, AI tells, vocabulary
│   ├── 01-decision-architecture/
│   │   ├── AUTHORITY-MATRIX.md              # 4-tier decision authority (identity level)
│   │   └── TRADEOFF-RULES.md               # Value conflict resolution rules
│   └── 02-quality-standards/
│       ├── BY-OUTPUT-TYPE.md                # Pass criteria for 6 output types
│       └── ANTI-PATTERNS.md                 # 10 things that are "not us"
│
├── governance/                               # How agents operate (operational layer)
│   ├── AUTHORITY-MATRIX.md                  # Agent-specific 4-tier authority
│   ├── HARD-BOUNDARIES.md                   # 9 non-negotiable rules
│   ├── ESCALATION-PROTOCOLS.md              # When and how agents escalate
│   ├── POLICY-GENERATION.md                 # How governance grows from evidence
│   ├── DECISION-LEDGER-SPEC.md              # Append-only decision record format
│   ├── LEARNING-LOOP.md                     # Monthly governance evolution cycle
│   └── HUMAN-USAGE-POLICY.md               # Human-facing AI policy
│
├── gates/                                    # Quality validation (gate layer)
│   ├── INDEX.md                             # Gate architecture overview
│   ├── article-publication.md               # Editorial quality gate
│   ├── code-merge.md                        # Compound engineering gate
│   ├── consulting-deliverable.md            # Consulting quality gate
│   ├── social-media-publication.md          # Social media gate
│   └── .holdouts/                           # Hidden test scenarios (23 total)
│       ├── article-publication-holdouts.md
│       ├── code-merge-holdouts.md
│       ├── consulting-deliverable-holdouts.md
│       └── social-media-publication-holdouts.md
│
├── specs/                                    # Workflow specifications (L2)
│   ├── article-production-2026-04-01-1440.md
│   ├── compound-engineering-2026-04-01-1440.md
│   ├── consulting-engagement-2026-04-01-1440.md
│   └── podcast-production-2026-04-01-1440.md
│
├── agents/                                   # Agent configurations (deployment layer)
│   ├── INDEX.md                             # Agent registry with authority tier summary
│   ├── editorial-quality/                   # Article review agent
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   ├── self-review-checklist.md
│   │   ├── config-anthropic-sdk.py          # Anthropic Agent SDK export
│   │   ├── config-openai-sdk.json           # OpenAI Agents SDK export
│   │   ├── config-crewai.yaml              # CrewAI export
│   │   └── config-openclaw.yaml            # OpenClaw export
│   ├── compound-engineering/                # Code development agent
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   ├── self-review-checklist.md
│   │   ├── config-anthropic-sdk.py
│   │   ├── config-openai-sdk.json
│   │   ├── config-crewai.yaml
│   │   └── config-openclaw.yaml
│   ├── consulting-pm/                       # Client engagement agent (Claudie)
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   ├── self-review-checklist.md
│   │   ├── config-anthropic-sdk.py
│   │   ├── config-openai-sdk.json
│   │   ├── config-crewai.yaml
│   │   └── config-openclaw.yaml
│   ├── content-distribution/                # Social media agent
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   ├── self-review-checklist.md
│   │   ├── config-anthropic-sdk.py
│   │   ├── config-openai-sdk.json
│   │   ├── config-crewai.yaml
│   │   └── config-openclaw.yaml
│   └── product-gm/                          # Full-stack product GM agent
│       ├── system-prompt.md
│       ├── tool-permissions.md
│       ├── self-review-checklist.md
│       ├── config-anthropic-sdk.py
│       ├── config-openai-sdk.json
│       ├── config-crewai.yaml
│       └── config-openclaw.yaml
│
├── adoption/                                 # Team maturity + sprint plans
│   ├── maturity-ladder-2026-04-01-1440.md   # 19 people assessed (Level 0-3)
│   ├── maturity-visibility.md               # How adoption is made visible
│   ├── sprint-2026-04-01-1440.md            # Internal + consulting sprint designs
│   └── sprint-measurement.md                # Measurement template
│
└── evolution/                                # Living governance loop
    ├── audit-2026-04-01-1440.md             # Baseline evolution audit
    ├── decision-ledger.md                   # Initialized decision record
    └── gate-telemetry.jsonl                 # Holdout evaluation telemetry
```

### `CLAUDE.md` — Governance Auto-Loading

The root `CLAUDE.md` uses `@imports` to load mission, values, and hard boundaries into every Claude Code session automatically.

### `.claude/` — Claude Code Integration

```
.claude/
├── agents/                                  # Sub-agent registrations (invokable via @name)
│   ├── editorial-quality.md                 # @editorial-quality
│   ├── compound-engineering.md              # @compound-engineering
│   ├── consulting-pm.md                     # @consulting-pm
│   ├── content-distribution.md              # @content-distribution
│   └── product-gm.md                        # @product-gm
└── skills/                                  # Governance operation skills
    ├── org-record-decision/SKILL.md         # /org-record-decision
    ├── org-novel-situation/SKILL.md         # /org-novel-situation
    ├── org-voice-check/SKILL.md             # /org-voice-check
    ├── org-gate-review/SKILL.md             # /org-gate-review
    └── org-values-check/SKILL.md            # /org-values-check
```

### `research/` — Reference Material

- `article-source-material.md` — Statistics and context for the article
- `dan-shipper-style-guide.md` — 389-line writing style profile built from analyzing Dan's articles
- `session-narrative.md` — Full session narrative of the 14-skill run
- `session-statistics.md` — Detailed output statistics by category
- `session-self-critique.md` — Self-assessment and quality analysis
- `chain-of-thought-insights.md` — Insights from the research phase
- `on-every-insights.md` — Research extractions about Every
- `source-code-insights.md` — Technical research extractions

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

AGENT-PRIMER.md distills ~7,000 lines of specification into 206 actionable operating rules any agent can load (33:1 compression). CLAUDE.md with @imports so governance auto-loads at session start. Five invokable `/org-*` skills for governance operations. Five Claude Code sub-agents registered for direct invocation via `@agent-name`.

## Key Insight

The hardest part of AI-first org design is not the framework. It's the excavation. Articulating implicit organizational knowledge ("what does 'taste' actually mean when you have to encode it for an agent?") is a genuinely difficult intellectual exercise. The 63-article research phase was the investment that made everything downstream credible.

## How It Was Made

One Claude Code session ran the complete 14-skill AI-First Org Design Kit, acting as Every's CEO based on research into 63 published articles. The session produced all artifacts without human intervention between phases, then underwent two revision passes for quality and structural conformance.

## The Plugin

The AI-First Org Design Kit is available on the [Synapti Marketplace](https://github.com/synaptiai/synapti-marketplace): [ai-first-org-design-kit](https://github.com/synaptiai/synapti-marketplace/tree/main/plugins/ai-first-org-design-kit)

Install via the [Synapti Marketplace](https://github.com/synaptiai/synapti-marketplace) in Claude Code, then run `/ai-first-kit` to start.

The conceptual foundation: [The Specification Economy](https://medium.com/@danielbentes/the-specification-economy-77f7d2297c37)