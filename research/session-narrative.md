# Session Narrative: Building Every's Organizational Genome with the AI-First Org Design Kit

## What Happened

A single Claude Code session ran the complete 13-skill AI-First Org Design Kit for Every Inc, acting as CEO Dan Shipper. The session produced 50 files totaling 11,907 lines of structured organizational design -- from coordination audit through evolution auditor -- without human intervention between phases.

## Timeline

### Phase 0: Deep Research (~45 minutes)

The session began with a comprehensive research sprint. The user requested that the agent act as Every's CEO and run the entire ai-first-kit process end-to-end. 

**Research approach:**
1. **Sitemap crawl** — Fetched `every.to/sitemaps/pages.xml` and discovered 2,242 URLs across 30+ columns in 5 sitemap files.
2. **Company research** — 3 parallel agents researched Every's business model, team, products, and Dan Shipper's philosophy via web search and direct page fetches.
3. **Newsletter deep-dive** — 3 more parallel agents fetched and extracted insights from 60+ articles across Chain of Thought (Dan's column), Source Code (engineering), and On Every (company updates). This was the critical research investment that enabled authentic CEO-voice answers later.
4. **Plugin analysis** — 1 agent explored the ai-first-kit plugin structure to map all 13 skills, their order, dependencies, and artifact formats.

**Key research outputs:**
- `research/chain-of-thought-insights.md` — 542 lines from 20 Dan Shipper articles
- `research/source-code-insights.md` — 986 lines from 20 engineering articles
- `research/on-every-insights.md` — 869 lines from 23 company update articles/pages

The research phase was initially insufficient -- the user correctly pushed back that newsletter content contains deep organizational detail that surface-level web research misses. This led to the second wave of 60+ article fetches.

### Phase 1: Coordination Audit

**Skill:** `coordination-audit`
**Duration of artifact creation:** ~5 minutes

The audit quantified Every's time allocation across 5 core workflows:

| Workflow | Specification | Coordination | Execution |
|----------|:---:|:---:|:---:|
| Article production | 45% | 20% | 35% |
| Compound engineering | 50% | 15% | 35% |
| Consulting delivery | 40% | 35% | 25% |
| Podcast production | 30% | 25% | 45% |
| Design rotation | 30% | 40% | 30% |
| **Company average** | **40%** | **27%** | **33%** |

**Key finding:** Every is already near AI-first target allocation (40-50% specification). The 27% coordination has ~10-12 percentage points that could be encoded. Top encoding candidate: design request intake at ~40 hours/month.

### Phase 2: Org Genome Builder

**Skill:** `org-genome-builder`
**Duration:** ~10 minutes

This was the most critical phase. The agent answered 11 Socratic questions as Dan Shipper, drawing on research to articulate Every's tacit organizational knowledge. Produced 7 genome files:

- **MISSION.md** — Operational mission ("we write, build, and teach AI"), who we serve ("high-taste AI early adopters in the allocation economy"), explicit exclusions
- **VALUES.md** — 5 values encoded as decision rules with conflict resolution: (1) Taste Over Process, (2) Ship and Iterate, (3) Builder Credibility (absolute tiebreaker), (4) Generalist Advantage, (5) Play as Strategy
- **VOICE.md** — Communication norms, formality gradient, words we use/avoid, AI tells to reject, three rigor tests
- **AUTHORITY-MATRIX.md** — 4-tier decision authority from the genome perspective
- **TRADEOFF-RULES.md** — 5 specific value conflict scenarios with resolution rules
- **BY-OUTPUT-TYPE.md** — Quality standards for 6 output types (articles, code, consulting, podcast, social, product copy)
- **ANTI-PATTERNS.md** — 10 organizational anti-patterns with explanations

### Phase 3: Political Navigator

**Skill:** `political-navigator`
**Duration:** ~8 minutes

Mapped power dynamics across 9 stakeholders. Key insight: Every's transformation risk is LOW because the CEO is driving it, the org is flat, incentives already align, and no genuine blockers exist.

Notable reframes designed:
- Kate Lee: Approval Gate Holder → Quality Architect
- Kieran Klaassen: Process Owner → Workflow Designer
- Natalia Quintero: Information Broker → Knowledge Encoder
- Katie Parrott: Execution Expert → Specification Authority

### Phase 4: Quality Gate Designer

**Skill:** `quality-gate-designer`
**Duration:** ~8 minutes

Designed 4 quality gates with 23 holdout scenarios:
1. **Article Publication** — 8 pass criteria across 2 tiers, 7 holdout scenarios
2. **Code Merge** — 9 pass criteria across 3 tiers, 6 holdout scenarios
3. **Consulting Deliverable** — 9 pass criteria across 3 tiers, 5 holdout scenarios
4. **Social Media Publication** — 6 pass criteria across 2 tiers, 5 holdout scenarios

Holdout scenarios stored separately in `gates/.holdouts/` to prevent executing agents from gaming visible criteria.

### Phases 5-6: Specifications + Roles (Parallel)

**Skills:** `specification-writer` + `role-value-mapper`
**Duration:** ~7 minutes (run in parallel via subagents)

**4 workflow specifications** written (L2 layer), each passing the Stranger Test:
- Article production pipeline (pitch → publication → social distribution)
- Compound engineering feature cycle (Plan → Work → Review → Compound)
- Consulting engagement delivery (onboarding → training → ongoing support)
- Podcast production (guest selection → recording → distribution)

**14 roles mapped** using the Three-Variable Model, decomposing each into Specification, Coordination, Execution, and AI Delegation percentages.

### Phases 7 + 9: Governance + Maturity Ladder (Parallel)

**Skills:** `governance-architect` + `maturity-ladder`
**Duration:** ~8 minutes (parallel)

**6 governance documents** produced:
- AUTHORITY-MATRIX.md — 4-tier agent decision authority with agent-type specifics
- HARD-BOUNDARIES.md — 9 non-negotiable boundaries with violation protocol
- ESCALATION-PROTOCOLS.md — 5 trigger categories, domain routing, escalation format
- POLICY-GENERATION.md — How governance grows from operational evidence
- DECISION-LEDGER-SPEC.md — Append-only decision record format
- LEARNING-LOOP.md — Monthly governance evolution cycle

**Maturity ladder** assessed 19 team members:
- 9 at Level 3 (Transformative — 47%)
- 7 at Level 2 (Adoptive — 37%)
- 2 at Level 1-2 (Transitional — 11%)
- 1 at Level 1 (Capable — 5%)
- Organizational mean: 2.4 out of 3.0

### Phases 8 + 10 + 11: Operationalize + Sprints + Usage Policy (Parallel)

**Skills:** `operationalize` + `adoption-sprint-designer` + `usage-policy-writer`
**Duration:** ~5 minutes (parallel)

- **AGENT-PRIMER.md** — 179-line distillation of ~9,200 lines of source artifacts (51:1 compression)
- **ORG-DESIGN-DUMP** — 2,671-line full concatenation for archival
- **2 adoption sprint designs** — Internal "Level 2 to 3" sprint + consulting client template
- **HUMAN-USAGE-POLICY.md** — Human-facing AI policy with approved tools, data classification, risk reasoning

### Phases 12 + 13: Agent Builder + Evolution Auditor (Parallel)

**Skills:** `agent-builder` + `evolution-auditor`
**Duration:** ~7 minutes (parallel)

**4 agent configurations** built:
1. Editorial Quality Agent (reviews articles against rigor tests + AI tells)
2. Compound Engineering Agent (executes Plan→Work→Review→Compound loop)
3. Consulting PM Agent (formalizes Claudie — Natalia's AI PM)
4. Content Distribution Agent (formalizes Anthony's Claude+X API system)

**Evolution infrastructure** established:
- Baseline evolution audit with governance health metric targets
- Initialized decision ledger with 3 realistic example entries
- Monthly review cycle scheduled (first Monday, Dan + Brandon required)

### Operationalize Re-Run

After all 13 phases, the `/operationalize` skill was run again to regenerate the AGENT-PRIMER.md incorporating all artifacts. This also generated:
- `.claude/CLAUDE.md` with @imports (MISSION, HARD-BOUNDARIES, VALUES auto-loaded at session start)
- 5 Claude Code governance skills (`/org-record-decision`, `/org-novel-situation`, `/org-voice-check`, `/org-gate-review`, `/org-values-check`)

### Quality Audit + Fixes

A final audit pass identified and fixed:
- **Brandon Gell's name** hallucinated as "Brandon Smithwick" in 3 governance files (agent confabulation during subagent generation)
- **Sparkle's GM** incorrectly listed as Anukshi Mittal instead of Yash Poojary in escalation protocols
- Other minor issues documented (see `session-audit.md`)
