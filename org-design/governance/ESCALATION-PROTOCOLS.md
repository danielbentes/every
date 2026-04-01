# Escalation Protocols

*Every Inc -- Governance v1.0 -- 2026-04-01*

## Purpose

When agents encounter situations beyond their authority tier, they escalate to humans. This document defines when to escalate, who to escalate to, what information to surface, and what happens if the human does not respond.

Design principle: escalations should make the human's decision *faster*, not create busywork. Every escalation must contain enough context for a decision in under 2 minutes.

---

## Escalation Triggers

### Category 1: Novel Situations

The agent encounters a situation not covered by existing governance, authority matrix, or product-specific CLAUDE.md.

**Examples at Every:**
- A subscriber asks Plus One a question that touches consulting-grade advice (not just product support).
- A compound engineering agent encounters a dependency that requires access to a service it has never used.
- Claudie receives a client request that falls outside the defined engagement scope.
- Spiral's multi-agent writing loop produces output that the agent cannot confidently evaluate against the three rigor tests.

**Escalation urgency:** Standard (within 1 hour of detection).

---

### Category 2: Value Conflicts

The agent identifies a tension between two or more of Every's values and the tradeoff rules (TRADEOFF-RULES.md) do not provide a clear resolution.

**Examples at Every:**
- Builder credibility vs. ship-and-iterate: a consulting deliverable is good enough to ship on deadline but contains a recommendation the agent is not confident Every has tested internally.
- Taste vs. speed: Katie's AI tells detection flags an article as borderline, but the pipeline nudge system shows the article is already past deadline.
- GM autonomy vs. company consistency: a GM's agent wants to implement a feature that would change shared subscription infrastructure.

**Escalation urgency:** Standard (within 1 hour). Exception: if the conflict involves a hard boundary, escalate immediately.

---

### Category 3: Boundary Proximity

The agent is operating near (but not yet at) a hard boundary, and continued operation on its current trajectory may result in a boundary violation.

**Examples at Every:**
- An agent composing a consulting status report begins to include data that could identify a different client.
- A compound engineering agent's auto-fix (Tier 2) is growing in scope to the point where it is effectively a new feature, not a bug fix.
- A social media draft agent generates a post that makes a claim the agent cannot find backing experience for in Every's knowledge base.
- A Plus One agent conversation is drifting from product support toward business advice.

**Escalation urgency:** Elevated (within 15 minutes). Agent should pause the action that is approaching the boundary.

---

### Category 4: Failure Cascades

A Tier 1 or Tier 2 action has failed, the agent's retry/self-correction has also failed, and continued autonomous operation risks compounding the problem.

**Examples at Every:**
- A compound engineering work agent's auto-fix introduces a new test failure, and its second fix attempt introduces another.
- Claudie's status report generation pulls stale data and the automated data refresh also fails.
- Cora's email triage misclassifies a time-sensitive client email as low priority, and the correction logic also misjudges it.
- A 14-agent code review produces contradictory findings that the synthesizer cannot resolve.

**Escalation urgency:** Immediate. Agent halts all related autonomous actions until human intervenes.

---

### Category 5: External Stakeholder Involvement

Any situation where an external party (client, partner, subscriber, press, investor) is directly involved or affected and the action is not already covered by an explicit Tier 3 approval flow.

**Examples at Every:**
- A subscriber replies to a Plus One agent message with a complaint or sensitive personal information.
- A consulting client contacts Every through an unexpected channel (e.g., DM to a personal agent instead of through Claudie).
- A journalist or researcher contacts Every about AI practices and an agent is the first to receive the message.

**Escalation urgency:** Immediate. Agent acknowledges receipt ("I'll make sure the right person sees this") and routes to human. No substantive response.

---

## Escalation Targets by Domain

| Domain | Primary Escalation Target | Secondary (if primary unavailable) | Slack Channel |
|---|---|---|---|
| **Editorial** (articles, newsletter, podcast, AI tells) | Kate Lee (EIC) | Eleanor Warnock (Managing Editor) | #editorial |
| **Engineering** (compound engineering, code review, infrastructure) | Product GM who owns the codebase | Andrey (compound engineering lead) for cross-product | #engineering |
| **Consulting** (client work, Claudie, engagement scope) | Natalia Quintero (Head of Consulting) | Dan Shipper (CEO) | #consulting |
| **Product -- Spiral** | Danny Aziz (GM) | Dan Shipper | #spiral |
| **Product -- Cora** | Kieran (GM) | Dan Shipper | #cora |
| **Product -- Monologue** | Naveen (GM) | Dan Shipper | #monologue |
| **Product -- Sparkle** | Yash Poojary (GM) | Dan Shipper | #sparkle |
| **Design** | Lucas Crespo (Creative Director) | Daniel Rodrigues | #design |
| **Social media** | Anthony | Kate Lee | #social |
| **Plus One / subscriber agents** | Relevant product GM | Brandon Gell | #plus-one |
| **Company-wide / cross-domain** | Dan Shipper (CEO) | Brandon Gell | #leadership |
| **Financial** | Dan Shipper | N/A -- Dan only | DM to Dan |
| **Crisis / security** | Dan Shipper | Brandon Gell | DM to Dan + #leadership |

---

## Escalation Format

Every escalation must follow this format to enable a 2-minute decision. Agents must fill in all fields; "unknown" is acceptable but the agent must explain why it is unknown.

```
ESCALATION -- [URGENCY: Immediate / Elevated / Standard]

Agent: [Agent name, e.g., Claudie, R2-C2, Spiral compound review]
Domain: [Editorial / Engineering / Consulting / Product / Cross-domain]
Trigger category: [Novel / Value conflict / Boundary proximity / Failure cascade / External stakeholder]

SITUATION (2-3 sentences max):
[What happened, what the agent was doing, what went unexpected]

WHAT I NEED FROM YOU:
[Specific decision or action required -- not "please advise" but "approve/reject X" or "choose between A and B"]

OPTIONS:
A: [First option + expected outcome]
B: [Second option + expected outcome]
C: [Hold/do nothing + expected outcome]

MY ASSESSMENT:
[Which option the agent recommends and why, grounded in Every's values]

RELEVANT CONTEXT:
- Authority tier: [Current tier for this action]
- Hard boundary proximity: [Which boundary, if any, is nearby]
- Time sensitivity: [Deadline or consequence of delay]
- Related decisions: [Link to decision ledger entries if relevant]
```

### Format Rules

- **Be specific.** "Should I publish this article?" is better than "I need editorial guidance."
- **Present options.** The human should choose, not brainstorm.
- **State your recommendation.** Agents have context humans may lack; hiding the recommendation wastes time.
- **Include time sensitivity.** If there is no deadline, say so. If there is, state it explicitly.

---

## Time-Bound Defaults

When a human does not respond to an escalation within the SLA, the following defaults apply.

| Urgency Level | SLA | Default If No Response |
|---|---|---|
| **Immediate** | 1 hour | Agent halts all related actions. Escalates to secondary target. If secondary unavailable within 1 additional hour, escalates to Dan. |
| **Elevated** | 4 hours | Agent holds the action that triggered escalation. Other unrelated work continues. Reminder sent at 2-hour mark. |
| **Standard** | 24 hours | Agent continues other work. Reminder sent at 12-hour mark. If 24 hours pass with no response, agent logs the timeout in the decision ledger and moves on to other tasks. |

### Critical Default Rule

**No escalation default ever results in the agent taking the escalated action autonomously.** The defaults are always: hold, halt, or move on -- never "proceed anyway."

Exceptions:
- Tier 1 actions that were escalated due to uncertainty: if the human does not respond within 24 hours and the agent's confidence has increased (e.g., new information became available), the agent may re-assess and downgrade back to Tier 1. This re-assessment must be logged.

---

## Escalation Chains

For situations where the primary target cannot resolve the escalation alone.

### Editorial Chain
1. Kate Lee (EIC) -- editorial judgment, publication decisions
2. Dan Shipper -- if editorial decision has company-wide implications
3. Full editorial team discussion -- if the decision sets a new precedent

### Engineering Chain
1. Product GM -- decisions within their product
2. Andrey (compound engineering) -- cross-product or infrastructure decisions
3. Dan Shipper + affected GMs -- if the decision affects shared infrastructure or multiple products

### Consulting Chain
1. Natalia Quintero -- client-facing decisions, engagement scope
2. Dan Shipper -- financial implications, new engagement types
3. Natalia + Dan jointly -- decisions that affect consulting positioning or pricing

### Cross-Domain Chain
When an escalation touches multiple domains (e.g., a consulting client wants a feature in Spiral):
1. Primary: domain where the action would occur (e.g., Spiral GM for product changes)
2. Secondary: domain where the request originated (e.g., Natalia for consulting relationship)
3. Arbiter: Dan Shipper if the two domains disagree

---

## Escalation Hygiene

### What makes a good escalation
- Specific ask, not vague concern
- All relevant context included (not requiring the human to go dig)
- Recommendation included with reasoning
- Follows the format above

### What makes a bad escalation
- "FYI" with no decision needed (this should be a Tier 2 notification, not an escalation)
- Escalating routine Tier 1 decisions out of excessive caution
- Escalating without a recommendation ("what should I do?" with no options)
- Bundling multiple unrelated decisions into one escalation

### Anti-Pattern: Escalation Flooding
If an agent generates more than 5 escalations per day, the agent should:
1. Group related escalations into a single summary escalation.
2. Self-assess whether its authority tier assignments are too conservative.
3. Flag the pattern for the monthly governance review (potential signal that authority tiers need adjustment).

---

*Reviewed by: Dan Shipper, Brandon Gell*
*Next review: 2026-05-01 (monthly governance review cycle)*
*Governance version: 1.0*
