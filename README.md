# Every Inc: Organizational Genome

This repository contains the complete output of running the [AI-First Org Design Kit](https://github.com/SynaptiAI/ai-first-org-design-kit) on Every Inc, a ~20-person media-software-consulting company that writes about AI, builds AI tools, and teaches companies to adopt AI.

**Article:** [I Encoded Every's Entire Operating System Into 52 Files an AI Agent Can Read](article.md)

## What's Here

### `org-design/` — The Complete Organizational Specification

52 structured markdown files produced by running 13 skills end-to-end:

```
org-design/
├── AGENT-PRIMER.md                          # 206-line distilled operating guide for agents
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
│   ├── INDEX.md                             # Agent registry
│   ├── editorial-quality/                   # Article review agent
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   └── self-review-checklist.md
│   ├── compound-engineering/                # Code development agent
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   └── self-review-checklist.md
│   ├── consulting-pm/                       # Client engagement agent (Claudie)
│   │   ├── system-prompt.md
│   │   ├── tool-permissions.md
│   │   └── self-review-checklist.md
│   └── content-distribution/                # Social media agent
│       ├── system-prompt.md
│       ├── tool-permissions.md
│       └── self-review-checklist.md
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

### `.claude/` — Claude Code Integration

```
.claude/
├── CLAUDE.md                                # @imports for auto-loading governance
└── skills/
    ├── org-record-decision/SKILL.md         # /org-record-decision
    ├── org-novel-situation/SKILL.md         # /org-novel-situation
    ├── org-voice-check/SKILL.md             # /org-voice-check
    ├── org-gate-review/SKILL.md             # /org-gate-review
    └── org-values-check/SKILL.md            # /org-values-check
```

### `research/` — Reference Material

- `dan-shipper-style-guide.md` — 389-line writing style profile built from analyzing Dan's articles
- `article-source-material.md` — Statistics and context for the article

### `archive/` — Process Documentation

Session narrative, statistics, quality audits, conformance checks, and raw research extractions from the exercise. Included for transparency about how the artifacts were produced.

## How It Was Made

One Claude Code session ran the complete 13-skill AI-First Org Design Kit, acting as Every's CEO based on research into 63 published articles. The session produced all artifacts without human intervention between phases, then underwent two revision passes for quality and structural conformance.

## The Plugin

The AI-First Org Design Kit is available at: https://github.com/SynaptiAI/ai-first-org-design-kit

Install via the Synapti Marketplace in Claude Code, then run `/ai-first-kit` to start.
