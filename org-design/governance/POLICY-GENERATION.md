# Policy Generation Protocol

*Every Inc -- Governance v1.0 -- 2026-04-01*

## Purpose

Governance at Every is not a static document set. As agents encounter novel situations, governance must grow to cover them -- but it must grow through evidence and human judgment, not through agents unilaterally expanding their own authority.

This document defines how new governance policies are proposed, reviewed, and adopted. It is the mechanism through which Every's agent governance stays current without becoming bureaucratic.

Design principle: governance should grow at the pace of operational learning, not at the pace of committee meetings. But every growth step requires human approval.

---

## When Policy Generation Triggers

An agent should draft a candidate policy when any of the following occur:

### 1. Repeated Escalations on the Same Pattern

The agent has escalated the same type of situation 3+ times in 30 days, and the human's decision was consistent each time. This is a signal that the pattern is stable enough to encode.

**Example at Every:** Claudie escalates to Natalia every time a consulting client asks about a topic adjacent to but outside the defined engagement scope. Natalia consistently says "offer a brief answer and note that a deeper dive would be a new engagement." After 3 instances, Claudie should draft a candidate policy: "When clients ask adjacent-scope questions, provide a brief answer (max 2 paragraphs) and note that a deeper exploration would require a scope adjustment."

### 2. Novel Situation with No Governance Coverage

The agent encounters a situation where:
- The authority matrix does not clearly assign a tier
- No hard boundary applies
- No tradeoff rule resolves the ambiguity
- The agent had to escalate as a result

**Example at Every:** A Plus One subscriber agent in a client Slack channel receives a question about a competitor's product. No existing governance covers how agents should discuss competitors. The agent escalates, the human provides guidance, and the agent drafts a candidate policy for competitor mentions.

### 3. Human Overrides an Agent's Tier Assessment

An agent assessed a decision at Tier 2 (autonomous + notify), but the human reviewing the notification corrects it to Tier 3 (human-in-loop) -- or vice versa. This indicates the authority matrix may need adjustment.

**Example at Every:** A compound engineering agent auto-fixes a bug (Tier 2) that turns out to involve a security-sensitive code path. The product GM says "that class of fix should always be Tier 3." The agent drafts a candidate policy: "Auto-fixes touching authentication, authorization, or encryption code paths require human-in-loop approval."

### 4. Value Conflict Resolution Creates Precedent

When a human resolves a value conflict that is not covered by TRADEOFF-RULES.md, that resolution should be captured as a candidate rule.

**Example at Every:** Kate Lee decides that podcast show notes (which are less prominent than articles but still public-facing) require editorial review but not the full three rigor tests. This creates a new tradeoff resolution: "Podcast show notes: editorial review required, abbreviated quality gate (AI tells detection + editor scan, not full three rigor tests)."

---

## Candidate Policy Format

Agents draft candidate policies using this structure:

```
CANDIDATE POLICY -- [date]

Proposed by: [Agent name]
Domain: [Editorial / Engineering / Consulting / Product / Cross-domain]
Governance document affected: [AUTHORITY-MATRIX / HARD-BOUNDARIES / ESCALATION-PROTOCOLS / TRADEOFF-RULES / other]

TRIGGER PATTERN:
[What recurring situation prompted this proposal -- include decision ledger references]

PROPOSED POLICY:
[The specific rule, written as an agent instruction. Must be concrete and testable.]

RATIONALE:
[Why this policy is warranted. Reference Every's values where applicable.]

EVIDENCE:
- [Decision ledger entry 1: date, situation, human decision]
- [Decision ledger entry 2: date, situation, human decision]
- [Decision ledger entry 3: date, situation, human decision]
(Minimum 3 entries for pattern-based proposals. Novel situations may have 1.)

ALTERNATIVES CONSIDERED:
- [Alternative A and why it was not preferred]
- [Alternative B and why it was not preferred]

IMPACT ASSESSMENT:
- Agents affected: [which agents or agent types]
- Authority tier change: [if any tier would shift, specify from/to]
- Hard boundary change: [if a boundary would be added, removed, or modified]
- Risk if adopted: [what could go wrong]
- Risk if not adopted: [what continues to go wrong without this policy]

RECOMMENDED REVIEWER: [Human who should approve, based on domain]
```

---

## Routing Rules

Candidate policies route to the appropriate human based on the domain and governance document affected.

| Governance Document Affected | Primary Reviewer | Secondary Reviewer |
|---|---|---|
| AUTHORITY-MATRIX | Dan Shipper + Brandon Gell | Affected domain lead |
| HARD-BOUNDARIES | Dan Shipper + affected boundary stakeholder (Kate for editorial, Natalia for client data) | Brandon Gell |
| ESCALATION-PROTOCOLS | Brandon Gell | Dan Shipper |
| TRADEOFF-RULES (editorial) | Kate Lee | Dan Shipper |
| TRADEOFF-RULES (product) | Relevant product GM | Dan Shipper |
| TRADEOFF-RULES (consulting) | Natalia Quintero | Dan Shipper |
| Product-specific CLAUDE.md | Product GM (sole authority) | N/A |
| New governance document needed | Dan Shipper | Brandon Gell |

---

## Review Process

### Step 1: Agent Drafts Candidate Policy
- Agent generates the candidate policy in the format above.
- Agent posts it to the #governance Slack channel (or creates a Linear ticket tagged `governance`).
- Agent notifies the recommended reviewer via Slack DM.

### Step 2: Human Reviews
- Reviewer has 7 days to review. This is not urgent -- governance grows deliberately.
- Reviewer may: **Approve**, **Modify and Approve**, **Reject with Reason**, or **Defer to Weekly Review**.
- If the reviewer modifies the policy, they annotate what changed and why.

### Step 3: Adoption
- **Approved** policies are integrated into the relevant governance document by the agent, with the reviewer confirming the integration.
- The decision ledger records: policy ID, date adopted, proposing agent, approving human, governance document updated.
- All agents operating under the affected governance document receive the update (via CLAUDE.md refresh or equivalent mechanism).

### Step 4: Announcement
- New policies are announced in the weekly all-hands (the cultural ritual that is never skipped).
- Format: "New governance policy: [one-sentence summary]. Proposed by [agent], approved by [human]. Now in [document]."

---

## Weekly Governance Review

**Cadence:** Every Monday, as part of Dan + Brandon's weekly operating review.
**Duration:** 15-30 minutes.
**Attendees:** Dan Shipper, Brandon Gell. Others invited when their domain is affected.

**Agenda:**
1. **Pending candidate policies** -- review any policies that were deferred or not yet reviewed.
2. **Escalation patterns** -- are any agents escalating too much? Too little? Patterns suggesting tier adjustment?
3. **Decision ledger highlights** -- any surprising or concerning decisions logged in the past week?
4. **Hard boundary stress tests** -- any near-violations logged? Do boundaries need clarification?
5. **Governance debt** -- any known gaps that need candidate policies but no agent has proposed one?

**Output:** Updated governance documents (if policies are approved), notes posted to #governance.

---

## Governance Anti-Patterns

### Policy Proliferation
If the governance document set grows beyond what an agent can reasonably hold in context, policies must be consolidated. The monthly governance review (see LEARNING-LOOP.md) includes a consolidation check.

**Signal:** More than 5 new policies adopted in a single month. This suggests either the original governance was too sparse (expected in v1.0) or agents are over-encoding edge cases.

### Premature Encoding
A single instance of a novel situation is not sufficient evidence for a permanent policy. The minimum evidence bar is 3 consistent human decisions on the same pattern.

**Exception:** If the novel situation involves a hard boundary near-miss, a single instance is sufficient to warrant a clarifying policy.

### Agent Self-Authorization
An agent must never draft a candidate policy that expands its own authority tier without the proposal being reviewed by a human who is NOT the agent's primary user. R2-C2 cannot propose expanding Dan's agents' autonomy without Brandon reviewing. Claudie cannot propose expanding consulting agent authority without Dan reviewing.

### Governance as Bureaucracy
If team members start experiencing governance as overhead rather than enablement, that is a critical signal. Every's culture values builder credibility and ship-and-iterate. Governance exists to enable confident shipping, not to slow it down. If it is slowing things down, the monthly review must address the friction.

---

*Reviewed by: Dan Shipper, Brandon Gell*
*Next review: 2026-05-01 (monthly governance review cycle)*
*Governance version: 1.0*
