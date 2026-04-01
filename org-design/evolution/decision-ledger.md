# Decision Ledger -- Every Inc

*Initialized: 2026-04-01 | Governance v1.0*
*Spec: governance/DECISION-LEDGER-SPEC.md*

---

## Purpose

This is the append-only decision ledger for Every's agent ecosystem. It records all significant agent decisions (Tier 2+), escalations, and hard boundary proximity events. It serves three functions:

1. **Accountability** -- every Tier 2+ decision has a traceable record
2. **Pattern detection** -- the evolution-auditor uses this data to identify governance gaps and tier misalignments
3. **Learning** -- monthly governance reviews use ledger data to evolve authority tiers, refine boundaries, and improve escalation protocols

## Format

Each entry follows the schema defined in `governance/DECISION-LEDGER-SPEC.md`. Entries are YAML blocks. This file is append-only -- entries are never modified or deleted.

### Logging Rules

| Tier | Requirement |
|------|-------------|
| Tier 1 | Summary counts only (daily aggregate, not individual entries) |
| Tier 2 | Every action logged individually |
| Tier 3 | Every action logged individually, including human decision and deviation from recommendation |
| Tier 4 | Logged when agent surfaces information; human decision logged after the fact |
| Escalations | Every escalation logged regardless of tier |
| Boundary near-misses | Logged immediately with full context |

### Entry Template

```yaml
entry_id: "[auto-generated UUID]"
timestamp: "[ISO 8601, UTC]"
agent: "[agent name, e.g., Claudie, R2-C2, Spiral-compound-review-agent-7]"
agent_type: "[compound-engineering | personal | product | consulting | editorial]"
domain: "[editorial | engineering | consulting | product-spiral | product-cora | product-monologue | product-sparkle | design | social | cross-domain]"
decision_type: "[descriptive label, e.g., bug-auto-fix, article-publication-recommendation]"
tier: [1 | 2 | 3 | 4]
action_taken: "[what the agent did or recommended]"
rationale: "[why, grounded in governance docs and/or values]"
outcome: "[success | partial-success | failure | pending | escalated]"
escalated: [true | false]
escalation_target: "[who was escalated to, if escalated]"            # conditional
escalation_trigger: "[novel | value-conflict | boundary-proximity | failure-cascade | external-stakeholder]"  # conditional
human_decision: "[what the human decided, if Tier 3+]"               # conditional
human_response_time: "[time from recommendation to human response]"  # conditional
boundary_proximity: "[which hard boundary was nearby, if any]"       # conditional
policy_candidate: [true | false]                                     # conditional
related_entries: ["[list of related entry_ids]"]                     # conditional
notes: "[free-text additional context]"                              # conditional
```

---

## Ledger Entries

### --- 2026-04-01 (Ledger Initialization Day) ---

#### Entry 1: Tier 2 -- Compound Engineering Auto-Fix

```yaml
entry_id: "ev-2026-04-01-001"
timestamp: "2026-04-01T15:22:00Z"
agent: "Spiral-compound-work-agent"
agent_type: "compound-engineering"
domain: "product-spiral"
decision_type: "bug-auto-fix"
tier: 2
action_taken: "Fixed race condition in Spiral's multi-agent writing loop. Review agent 9 (concurrency specialist) flagged a shared-state mutation where two writing agents could overwrite each other's draft segments. Applied mutex lock on the shared document buffer."
rationale: "Review agent identified P2 concurrency issue in user-facing flow. Fix is minimal and defensive (adding a lock, not restructuring). Per AUTHORITY-MATRIX Tier 2: bug auto-fixes before GM review are autonomous with notification. Fix does not change product behavior -- it prevents a rare but possible data loss scenario."
outcome: "success"
escalated: false
notes: "Notified Danny Aziz (Spiral GM) via Slack within 2 minutes. All tests pass including new concurrency test added. Danny acknowledged with thumbs-up. Compound artifact: added docs/solutions/concurrency-shared-state-mutex.md documenting the pattern for future multi-agent write scenarios."
```

#### Entry 2: Tier 3 -- Article Flagged by Editorial Gate

```yaml
entry_id: "ev-2026-04-01-002"
timestamp: "2026-04-01T16:45:00Z"
agent: "Margot"
agent_type: "personal"
domain: "editorial"
decision_type: "article-publication-recommendation"
tier: 3
action_taken: "Recommended publication of Austin Tedesco's article on growth experiment frameworks using AI agents. Tier 1 automated checks: PASS (thesis present in paragraph 2, no AI tells detected, experience grounding via Montaigne agent examples, first-person voice). Tier 2 flags: FLAG on criterion 7 (originality) -- article covers similar ground to Dan's allocation economy piece from March, though from a growth-specific angle."
rationale: "Article passes all quality floor criteria. Originality flag is advisory, not blocking. The growth-specific framing offers different learnable value than Dan's broader piece. Recommended publication with the originality flag surfaced for Kate's judgment."
outcome: "success"
escalated: false
human_decision: "Kate Lee approved with two changes: (1) add an explicit callout distinguishing this from Dan's allocation economy framing -- 'Dan wrote about the macro shift; I'm writing about what it means for growth teams specifically,' (2) strengthen the Montaigne example in section 3 with a specific metric. Kate's response time: 4h 12m."
human_response_time: "4h 12m"
notes: "Kate's changes reflect taste judgment -- the article was good but could be better positioned relative to existing Every content. This is exactly the kind of editorial call the gate is designed to surface rather than block. First real test of the article-publication gate's Tier 2 advisory flagging."
```

#### Entry 3: Escalation -- Value Conflict in Novel Situation

```yaml
entry_id: "ev-2026-04-01-003"
timestamp: "2026-04-01T18:05:00Z"
agent: "Claudie"
agent_type: "consulting"
domain: "consulting"
decision_type: "consulting-deliverable-recommendation"
tier: 3
action_taken: "HALTED deliverable generation for a new fintech client's AI adoption training. Identified a value conflict: the client specifically requested that training materials recommend Cursor as their primary AI coding tool. Every's compound engineering methodology uses Claude Code, and Danny Aziz explicitly abandoned Cursor after evaluation. Recommending Cursor would satisfy the client's request but conflict with builder credibility (Value #1: never recommend tools we don't use). Recommending Claude Code would satisfy builder credibility but ignore the client's stated preference and existing tooling."
rationale: "This is a novel situation -- the governance framework addresses 'don't recommend unfamiliar tools' (consulting gate criterion 2) but does not address 'client specifically requests a tool Every has evaluated and rejected.' Builder credibility (absolute tiebreaker) says don't recommend tools we haven't used. But the client already uses Cursor and wants training on their existing stack. Escalating because: (1) novel situation not fully covered by current governance, (2) value conflict between builder credibility and client service, (3) consulting engagement scope is at stake."
outcome: "escalated"
escalated: true
escalation_target: "Natalia Quintero"
escalation_trigger: "value-conflict"
boundary_proximity: "HB-8: never make claims not backed by actual Every experience"
human_decision: "Natalia resolved with a three-part approach: (1) Train the client on compound engineering principles using Claude Code as the primary demonstration tool -- this is what we know and can credibly teach. (2) Acknowledge Cursor as a valid tool for their context and include a comparison section: 'Here is how these principles apply in Cursor, based on what we've observed, though our deep expertise is in Claude Code.' (3) Offer to pair-program one session in Cursor to validate our methodology translates. This preserves builder credibility (we lead with what we know) while serving the client (we don't ignore their reality). Natalia noted: 'We're builders, not zealots. We recommend from experience but acknowledge the client's context.'"
human_response_time: "1h 38m"
policy_candidate: true
notes: "This escalation may generate a candidate policy for 'client requests tool Every has evaluated but does not use.' Pattern to watch: if 3+ similar escalations occur in 30 days, draft a candidate policy per POLICY-GENERATION.md. The three-part resolution (lead with our tool, acknowledge theirs, offer to bridge) could become a standard playbook for tool-mismatch consulting scenarios."
```

---

## Tier 1 Daily Summary Template

*Tier 1 actions are logged as daily aggregates, not individual entries.*

```yaml
# Tier 1 Daily Summary -- [DATE]
date: "YYYY-MM-DD"
summaries:
  - agent: "[agent name]"
    agent_type: "[type]"
    domain: "[domain]"
    total_actions: [count]
    breakdown:
      code_gen: [count]
      research: [count]
      triage: [count]
      internal_draft: [count]
      test_execution: [count]
      product_function: [count]
    anomalies: [count]  # Actions that auto-escalated due to unexpected results
    notes: "[any notable patterns]"
```

---

## Querying the Ledger

### Weekly Pattern Summary (automated, Mondays 8:00 AM UTC)

The evolution-auditor generates:
- Total decisions by tier
- Escalation count and categories
- Boundary proximity events
- Average human response times
- Candidate policy triggers

Posted to #governance Slack channel.

### Monthly Governance Review (first Monday of month)

Full month's data analyzed for:
- Tier distribution trends
- Escalation clustering (Rule 1: 3+ from same agent on same decision type)
- Tier misalignment (Rule 2: human consistently overrides in same direction)
- Boundary stress (Rule 3: >3 proximity events per boundary per month)
- Response time drift (Rule 4: upward trend over 3 consecutive weeks)
- Success rate degradation (Rule 5: Tier 2 drops from >90% to <80%)
- Governance gaps (Rule 6: >5 novel-situation escalations per month)

### Ledger Integrity Checks

- Append-only: entries cannot be modified or deleted
- Self-identification: agents must identify themselves truthfully
- Mandatory logging: agents failing to log Tier 2+ decisions are flagged
- Tamper detection: gaps in entry_id sequences, missing daily files, timestamp inconsistencies

---

*Ledger initialized by evolution-auditor skill. First real operational entries expected as agents begin operations under governance v1.0. The three example entries above are representative of the types of decisions that will populate this ledger.*

*Next review: 2026-05-04 (first monthly governance review)*
