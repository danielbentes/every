# Decision Ledger Specification

*Every Inc -- Governance v1.0 -- 2026-04-01*

## Purpose

The decision ledger is an append-only record of all significant agent decisions across Every's agent ecosystem. It serves three functions:

1. **Accountability:** Every Tier 2+ decision has a traceable record.
2. **Pattern detection:** The evolution-auditor skill uses ledger data to identify governance gaps, tier misalignments, and emerging risks.
3. **Learning:** Monthly governance reviews use ledger data to evolve authority tiers, refine boundaries, and improve escalation protocols.

Design principle: the ledger must be low-friction for agents to write to and high-value for humans to read from. Agents log automatically; humans query on demand.

---

## What Gets Logged

| Tier | Logging Requirement |
|---|---|
| **Tier 1 (Full Autonomy)** | Summary counts only. Daily aggregate: "R2-C2: 47 Tier 1 actions (23 code gen, 12 research, 8 triage, 4 draft)." Individual entries not required unless the action produced an anomaly. |
| **Tier 2 (Autonomous + Notify)** | Every action logged individually. This is the primary data source for governance evolution. |
| **Tier 3 (Human-in-Loop)** | Every action logged individually, including the human's decision and any deviation from the agent's recommendation. |
| **Tier 4 (Human-Only)** | Logged when the agent surfaces information. The human's decision is logged by the human (or their personal agent) after the fact. |
| **Escalations** | Every escalation logged, regardless of tier. Includes response time and resolution. |
| **Hard boundary near-misses** | Logged immediately with full context. These are high-signal events. |

---

## Entry Format

Each ledger entry follows this schema. Fields marked [required] must always be populated. Fields marked [conditional] are populated when applicable.

```yaml
entry_id: [required] # Auto-generated UUID
timestamp: [required] # ISO 8601, UTC
agent: [required] # Agent name (e.g., "Claudie", "R2-C2", "Spiral-compound-review-agent-7")
agent_type: [required] # One of: compound-engineering, personal, product, consulting, editorial
domain: [required] # One of: editorial, engineering, consulting, product-spiral, product-cora, product-monologue, product-sparkle, design, social, cross-domain
decision_type: [required] # Descriptive label (e.g., "bug-auto-fix", "client-status-report", "code-merge-approval")
tier: [required] # 1, 2, 3, or 4
action_taken: [required] # What the agent did or recommended
rationale: [required] # Why, grounded in governance docs and/or values
outcome: [required] # One of: success, partial-success, failure, pending, escalated
escalated: [required] # Boolean
escalation_target: [conditional] # Who was escalated to, if escalated
escalation_trigger: [conditional] # Category from ESCALATION-PROTOCOLS.md (novel, value-conflict, boundary-proximity, failure-cascade, external-stakeholder)
human_decision: [conditional] # What the human decided (Tier 3+), if different from agent recommendation
human_response_time: [conditional] # Time from escalation/recommendation to human response
boundary_proximity: [conditional] # Which hard boundary was nearby, if any (from HARD-BOUNDARIES.md)
policy_candidate: [conditional] # Boolean -- did this entry contribute to a candidate policy proposal?
related_entries: [conditional] # List of entry_ids for related decisions
notes: [conditional] # Free-text for additional context
```

### Example Entries

**Tier 2 -- Bug Auto-Fix:**
```yaml
entry_id: "a1b2c3d4-5678-90ab-cdef-111111111111"
timestamp: "2026-04-01T14:30:00Z"
agent: "Spiral-compound-work-agent"
agent_type: "compound-engineering"
domain: "product-spiral"
decision_type: "bug-auto-fix"
tier: 2
action_taken: "Fixed null pointer in markdown parser flagged by review agent 3. Applied defensive nil check."
rationale: "Review agent identified crash path in user-facing flow. Fix is minimal and defensive. Per AUTHORITY-MATRIX Tier 2: auto-fix before review."
outcome: "success"
escalated: false
notes: "Notified Danny via Slack. All tests pass."
```

**Tier 3 -- Article Publication:**
```yaml
entry_id: "b2c3d4e5-6789-01bc-defg-222222222222"
timestamp: "2026-04-01T16:00:00Z"
agent: "Margot"
agent_type: "personal"
domain: "editorial"
decision_type: "article-publication-recommendation"
tier: 3
action_taken: "Recommended publication of Katie's article on AI detection methods. AI tells check passed. Three rigor tests addressed in revision."
rationale: "Article meets editorial quality bar. No AI tells flags remaining after revision. Timely topic with reader interest signal from social engagement."
outcome: "pending"
escalated: false
human_decision: "Approved with minor headline change"
human_response_time: "3h 22m"
notes: "Kate requested headline change from 'How to Spot AI Writing' to 'The Tells That Give AI Away' -- taste call on voice."
```

**Escalation -- Boundary Proximity:**
```yaml
entry_id: "c3d4e5f6-7890-12cd-efgh-333333333333"
timestamp: "2026-04-01T10:15:00Z"
agent: "Claudie"
agent_type: "consulting"
domain: "consulting"
decision_type: "client-status-report"
tier: 2
action_taken: "Halted status report generation for Client B. Report draft contained a workflow pattern reference that could identify Client A."
rationale: "Hard boundary 4: never access or share client data across engagements. Report referenced 'a similar workflow we implemented for a fintech client' -- only one fintech client active."
outcome: "escalated"
escalated: true
escalation_target: "Natalia Quintero"
escalation_trigger: "boundary-proximity"
boundary_proximity: "HB-4: client data cross-engagement"
human_decision: "Remove the reference entirely. Good catch."
human_response_time: "45m"
policy_candidate: true
notes: "Contributing to candidate policy on anonymization standards for cross-client pattern references."
```

---

## Storage and Access

### Storage
- Ledger entries are stored as structured YAML/JSON in an append-only log.
- Location: `governance/ledger/` directory.
- One file per day: `YYYY-MM-DD.yaml`
- Files are append-only. Entries are never modified or deleted.
- Tier 1 daily summaries are stored in a separate file: `YYYY-MM-DD-tier1-summary.yaml`

### Access Permissions
- **Write:** All Every agents (each agent writes its own entries).
- **Read (full):** Dan Shipper, Brandon Gell, evolution-auditor skill.
- **Read (domain-filtered):** Each domain lead can read entries for their domain.
  - Kate Lee: editorial domain entries
  - Natalia Quintero: consulting domain entries
  - Product GMs: their own product domain entries
  - Lucas Crespo: design domain entries
- **Read (agent-filtered):** Each team member can read entries from their personal agent.
- **No external access.** Ledger data never leaves Every's internal systems.

### Retention
- Active ledger: rolling 90 days of full entries.
- Archive: entries older than 90 days are compressed and moved to archive. Pattern summaries are preserved; individual entries are available on request.
- Permanent retention: all hard boundary near-miss entries and all escalation entries.

---

## Review Cadence

### Weekly: Automated Pattern Summary
- Every Monday at 8:00 AM UTC, the evolution-auditor skill generates a pattern summary from the past week's ledger entries.
- Summary includes: total decisions by tier, escalation count and categories, boundary proximity events, average human response times, candidate policy triggers.
- Posted to #governance Slack channel for Dan + Brandon's weekly review.

### Monthly: Full Governance Review
- First Monday of each month.
- Dan Shipper + Brandon Gell review the full month's ledger data.
- Inputs: weekly pattern summaries, raw escalation entries, boundary near-miss entries, candidate policy proposals.
- Outputs: governance document updates, authority tier adjustments, new policies adopted.
- See LEARNING-LOOP.md for the full monthly review process.

### Quarterly: Trend Analysis
- Evolution-auditor skill produces a quarterly trend report.
- Tracks: tier distribution shifts, escalation volume trends, boundary stress patterns, governance growth rate.
- Presented at Every's quarterly planning (Dan + full leadership team).

---

## Pattern Detection Rules

The evolution-auditor skill runs these pattern detection rules against ledger data:

### Rule 1: Escalation Clustering
If 3+ escalations from the same agent on the same decision type occur within 30 days, flag for candidate policy generation (see POLICY-GENERATION.md).

### Rule 2: Tier Misalignment
If a human consistently overrides an agent's tier assessment in the same direction (e.g., agent says Tier 2, human says Tier 3, three times), flag the decision type for authority matrix review.

### Rule 3: Boundary Stress
If boundary proximity events for the same boundary exceed 3 per month, flag the boundary for clarification or the workflow for redesign.

### Rule 4: Response Time Drift
If average human response time for Tier 3 decisions trends upward over 3 consecutive weeks, flag as potential bottleneck. May indicate the human is overloaded or the tier assignment is wrong.

### Rule 5: Success Rate Degradation
If Tier 2 decision outcomes shift from >90% success to <80% over a rolling 30-day window, flag the agent or decision type for review. Autonomous decisions should have high success rates; degradation signals drift.

### Rule 6: Governance Gap
If novel-situation escalations (Category 1 from ESCALATION-PROTOCOLS.md) exceed 5 per month, flag as governance gap. The existing governance is not covering the operational reality.

---

## Ledger Integrity

- **Append-only.** Entries cannot be modified or deleted by agents.
- **Self-identification.** Agents must identify themselves truthfully. An agent cannot log an entry as another agent.
- **Mandatory logging.** Agents that fail to log Tier 2+ decisions are flagged in the weekly pattern summary as a governance compliance issue.
- **Tamper detection.** The evolution-auditor skill checks for gaps in entry_id sequences, missing daily files, and entries with timestamps inconsistent with their file dates.

---

*Reviewed by: Dan Shipper, Brandon Gell*
*Next review: 2026-05-01 (monthly governance review cycle)*
*Governance version: 1.0*
