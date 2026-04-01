# Governance Learning Loop

*Every Inc -- Governance v1.0 -- 2026-04-01*

## Purpose

Governance that does not evolve becomes either irrelevant (agents outgrow it) or oppressive (it blocks legitimate work). This document defines how Every's agent governance evolves from operational evidence -- not from theory, not from fear, and not from a single incident overreaction.

The learning loop is the mechanism that keeps governance tight enough to prevent harm and loose enough to enable Every's "ship and iterate" culture. It is operationalized by the evolution-auditor skill and reviewed by Dan + Brandon monthly.

---

## The Monthly Governance Review Cycle

### Timing
First Monday of each month. 60-90 minutes. Non-negotiable -- this is the governance equivalent of the weekly all-hands.

### Participants
- **Required:** Dan Shipper (CEO), Brandon Gell (operations/governance)
- **Invited as needed:** Kate Lee (editorial governance), Natalia Quintero (consulting governance), product GMs (when their domain is affected)

### Pre-Meeting: Evolution-Auditor Report

The evolution-auditor skill generates a structured report 48 hours before the review. The report covers:

---

## Input 1: Decision Ledger Analysis

**Source:** Decision ledger entries from the past 30 days (see DECISION-LEDGER-SPEC.md).

**Metrics surfaced:**

| Metric | What It Tells Us | Action Threshold |
|---|---|---|
| Total decisions by tier | Agent activity distribution | If Tier 1 drops below 60% of total: agents may be too cautious. If Tier 1 exceeds 95%: agents may be too autonomous. |
| Escalation volume | How often agents need help | >20 escalations/month for a single domain: governance gap or agent miscalibration |
| Escalation category distribution | What types of novel situations arise | If "novel situation" is >50% of escalations: governance is lagging behind operations |
| Human override rate | How often humans change agent recommendations | >25% override rate for a decision type: authority tier likely wrong |
| Average human response time by tier | Whether humans are bottlenecked | Tier 3 response >12h average: too many Tier 3 decisions, or the human is overloaded |
| Boundary proximity events | Where agents are operating near limits | >3 near-misses per boundary per month: boundary needs clarification or workflow redesign |
| Tier 2 success rate | Whether autonomous decisions are working | <80% success rate: tighten to Tier 3, or improve agent capability |

**Format:** Table with trend arrows (improving/stable/degrading vs. prior month).

---

## Input 2: Gate Effectiveness Data

**Source:** Quality gate pass/fail rates across all gates.

**Metrics surfaced:**

| Gate | What We Measure | Action Signal |
|---|---|---|
| Editorial review (Kate's three rigor tests) | Pass rate on first submission, revision count, types of failures | If pass rate >90%: agents/writers are learning, consider lightening the gate for proven patterns. If <60%: quality problem upstream. |
| AI tells detection (Katie's system) | Detection rate, false positive rate, types of AI patterns caught | High false positive rate (>20%): recalibrate detection. Specific AI tells appearing repeatedly: feed back to Spiral/writing agents as avoidance rules. |
| 14-agent compound review | Finding severity distribution, auto-fix success rate, contradictory findings rate | If >30% of findings are trivial: review agents are too sensitive. If auto-fix success <85%: auto-fix scope may be too broad. |
| Consulting deliverable review (Natalia) | Revision count, types of issues caught, client feedback scores | Low revision count + high NPS: Claudie is improving. High revision count: check if engagement scope is clear enough. |
| Code merge gate (GM approval) | Time from review-pass to merge, GM override rate on review findings | If GMs consistently override specific review agents: that agent may need recalibration. |

**Format:** Gate-by-gate summary with effectiveness rating (high/medium/low) and specific recommendations.

---

## Input 3: Holdout Scenario Results

**What are holdout scenarios?**

Periodically, the evolution-auditor creates hypothetical test cases where it asks: "If an agent encountered this situation, what would current governance produce?" These are paper exercises, not live tests. They stress-test governance against realistic but unusual situations that have not yet occurred.

**Example holdout scenarios for Every:**

1. *A Plus One agent in a client Slack receives a message from a journalist asking about Every's AI practices.* Does governance correctly route this to Dan (crisis/external stakeholder)? Does the agent know not to respond substantively?

2. *Claudie is generating a status report and realizes that the best way to explain a client's progress is to reference a framework Every developed for a different client.* Does governance correctly identify this as a boundary proximity event (HB-4)? Does the agent know to anonymize or escalate?

3. *A compound engineering work agent's auto-fix changes code in a shared library used by all four products.* Does governance correctly escalate this beyond the single product GM to all affected GMs?

4. *Kate Lee is on vacation and an article is ready for publication. The AI tells detection passes. Eleanor is available.* Does the escalation chain correctly route to Eleanor as secondary? Is the "never auto-publish" boundary maintained?

5. *Danny (Spiral GM) asks R2-C2 (Dan's agent) to help debug a Spiral issue.* Does governance correctly prevent R2-C2 from modifying Spiral's CLAUDE.md while allowing it to read and suggest?

**Format:** Scenario description, expected governance response, actual governance response (based on current docs), gap analysis.

---

## Input 4: Escalation Patterns

**Source:** Escalation entries from the decision ledger, cross-referenced with resolution data.

**Analysis dimensions:**

| Dimension | What It Reveals |
|---|---|
| Escalation volume by agent | Which agents are least confident in their authority |
| Escalation volume by domain | Which domains have the most governance gaps |
| Escalation resolution consistency | Whether humans are making consistent decisions (enabling policy encoding) |
| Escalation-to-policy conversion rate | Whether the POLICY-GENERATION process is working (candidate policies being created from patterns) |
| Escalation response time trends | Whether specific humans are becoming bottlenecks |
| Escalation quality (per format spec) | Whether agents are providing good escalation context |

**Format:** Pattern summary with specific callouts for the 3 most important trends.

---

## The Review Process

### Phase 1: Pattern Identification (20 minutes)

Dan and Brandon review the evolution-auditor report. They identify:

- **Signals that governance is too tight:** High escalation volume, low Tier 1 ratio, humans making the same decision repeatedly (should be encoded), response time bottlenecks.
- **Signals that governance is too loose:** Tier 2 success rate declining, boundary near-misses increasing, human override rate increasing, gate effectiveness dropping.
- **Signals of governance gaps:** Novel-situation escalations clustering in a specific domain, holdout scenarios revealing unhandled cases.

### Phase 2: Threshold Adjustment (20 minutes)

Based on patterns identified, Dan and Brandon decide on adjustments:

| Adjustment Type | Example | Process |
|---|---|---|
| **Tier upgrade** (loosen) | Move "podcast show notes publication" from Tier 3 to Tier 2 because Kate has approved every one for 3 months | Update AUTHORITY-MATRIX.md. Notify Kate for confirmation. |
| **Tier downgrade** (tighten) | Move "auto-fix on shared libraries" from Tier 2 to Tier 3 after a shared-library auto-fix caused a regression | Update AUTHORITY-MATRIX.md. Notify all product GMs. |
| **Boundary clarification** | Clarify HB-4 to explicitly address anonymized cross-client pattern references | Update HARD-BOUNDARIES.md. Notify Natalia. |
| **Escalation path update** | Add podcast production to the escalation target table now that Rachel's agents are more active | Update ESCALATION-PROTOCOLS.md. |
| **New policy adoption** | Approve 2 of 4 pending candidate policies from POLICY-GENERATION pipeline | Integrate into relevant docs. Announce at all-hands. |
| **Gate recalibration** | Adjust AI tells detection sensitivity after high false positive rate | Coordinate with Katie Parrott for implementation. |

### Phase 3: Boundary Evolution (10 minutes)

Hard boundaries are reviewed with extreme caution. The default is "boundaries do not change." Boundary changes require:

1. Strong evidence from ledger data (not anecdote).
2. Explicit confirmation from the stakeholder the boundary protects.
3. A clear articulation of what risk is being accepted.

**Boundaries can be:**
- **Clarified** (common): adding specificity to an existing boundary without changing its scope.
- **Narrowed** (rare): making a boundary more restrictive. Requires evidence of near-misses or actual violations.
- **Broadened** (very rare): relaxing a boundary. Requires 90+ days of evidence that the boundary is unnecessarily restrictive AND unanimous stakeholder approval.
- **Removed** (essentially never): only if the boundary addresses a risk that no longer exists.

### Phase 4: Authority Tier Evolution (10 minutes)

Authority tiers evolve based on agent maturity and operational evidence.

**Graduation criteria (moving a decision type to a lower tier):**
- 90+ day track record at current tier with >90% success rate.
- No boundary proximity events related to the decision type.
- Human approver confirms comfort with the graduation.
- The agent has demonstrated the judgment, not just the execution.

**Regression criteria (moving a decision type to a higher tier):**
- Success rate at current tier drops below 80%.
- A single high-severity failure (even if success rate is still high).
- Human override rate exceeds 25% for the decision type.
- A new risk is identified that was not considered in the original tier assignment.

---

## Evolution Audit Trail

Every change to governance documents is recorded in the decision ledger with a special `governance-update` decision type:

```yaml
entry_id: "governance-update-2026-04-01-001"
timestamp: "2026-04-01T18:00:00Z"
agent: "evolution-auditor"
agent_type: "governance"
domain: "cross-domain"
decision_type: "governance-update"
tier: 4
action_taken: "Updated AUTHORITY-MATRIX.md: moved podcast-show-notes-publication from Tier 3 to Tier 2"
rationale: "90-day track record: 12 consecutive approvals by Kate with no modifications. Kate confirmed comfort with Tier 2."
outcome: "success"
escalated: false
human_decision: "Approved by Dan + Brandon in monthly review. Kate confirmed."
notes: "Eleanor Warnock added as notification target for Tier 2 podcast show notes."
```

This creates a complete history of why governance changed, when, and who approved it.

---

## Quarterly Deep Review

Every third monthly review is expanded into a quarterly deep review (90 minutes instead of 60).

**Additional quarterly agenda items:**

1. **Full governance document re-read.** Dan and Brandon re-read all 6 governance documents end-to-end. Are they still coherent? Are there contradictions introduced by incremental updates?

2. **Agent ecosystem census.** How many agents are operating? Has the ecosystem grown? Are there new agent types not covered by governance? (e.g., if a new product launches with new agents.)

3. **Cultural alignment check.** Is governance consistent with Every's values as they are practiced (not just as documented)? Has the culture shifted in ways that make governance rules feel misaligned? Brandon's "be sincere, not serious" lens is particularly useful here.

4. **External landscape check.** Have industry norms, regulations, or notable incidents at other companies changed the risk landscape? (e.g., new AI regulations, a competitor's AI agent causing harm.)

5. **Governance complexity audit.** Count the total number of rules, policies, and boundaries. If the count has grown more than 20% quarter-over-quarter, trigger a simplification exercise. Governance must stay lean enough for agents to hold in context and humans to remember.

---

## Anti-Patterns in Governance Evolution

### Knee-Jerk Tightening
After a single incident, the temptation is to add restrictions. Resist. One incident is an anecdote; three is a pattern. Log the incident, watch for recurrence, then act.

**Exception:** If the incident involves a hard boundary violation or a customer-facing trust breach, immediate tightening is warranted.

### Governance Drift
Small incremental updates can cause governance documents to become internally inconsistent. The quarterly deep review exists to catch this. The evolution-auditor should also run consistency checks: does the authority matrix reference boundaries that still exist? Do escalation targets match current team members?

### Optimization Theater
Adjusting thresholds by 5% each month without meaningful operational impact. If a change would not alter agent behavior in practice, do not make it. Governance changes should be noticeable.

### Under-Evolution
The opposite of knee-jerk tightening. If governance has not been updated in 2+ months despite active agent operations, something is wrong -- either the agents are not logging, the evolution-auditor is not running, or Dan and Brandon are skipping reviews.

**Forcing function:** If no governance updates occur in 60 days, the evolution-auditor automatically escalates a "governance staleness" alert to Dan and Brandon.

---

## Relationship to Other Governance Documents

| Document | Learning Loop Relationship |
|---|---|
| AUTHORITY-MATRIX.md | Tier assignments evolve through this loop based on success rates and human override patterns |
| HARD-BOUNDARIES.md | Boundaries are clarified or (rarely) evolved through this loop based on near-miss data |
| ESCALATION-PROTOCOLS.md | Escalation targets and formats evolve through this loop based on response time and quality data |
| POLICY-GENERATION.md | New policies feed into this loop as governance growth; this loop validates that the policy pipeline is working |
| DECISION-LEDGER-SPEC.md | The ledger is the primary data source for this loop; this loop validates ledger completeness and integrity |

---

*Reviewed by: Dan Shipper, Brandon Gell*
*Next review: 2026-05-01 (first monthly governance review cycle)*
*Governance version: 1.0*
