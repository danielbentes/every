# Gate: Consulting Deliverable

## What It Replaces
Natalia Quintero's manual review of all client-facing consulting materials (training curricula, strategy assessments, custom tool deliverables, workshop materials). Currently 1-3 day turnaround per engagement touchpoint.

## Pass Criteria (visible to executing agent)

### Tier 1: Builder Credibility (blocking)
1. **Grounded in Every's experience:** Every recommendation references how Every (or a specific team member) has actually implemented it. No "organizations should consider..." without "Here's what happened when we tried..."
2. **No unfamiliar tools:** Does not recommend tools, frameworks, or practices Every hasn't used internally. If referencing a client-specific tool, clearly scoped as "for your context" not "our recommendation."
3. **No overselling:** Claims about AI capabilities are backed by demonstrated results. Time savings and productivity gains are based on measured outcomes, not projections.
4. **Client confidentiality:** Contains no information from other client engagements, even anonymized, unless the referenced client has given explicit permission.

### Tier 2: Quality and Relevance (blocking)
5. **Client-specific customization:** Materials are tailored to the client's industry (finance or tech), team size, AI maturity level (L1-L4), and specific use cases discussed during onboarding.
6. **Actionable within client constraints:** At least one recommendation can be implemented by the client within their first week without additional help from Every.
7. **Hands-on component:** Deliverable includes or references a hands-on building exercise — not just slides or documents. "We build together" is the consulting ethos.

### Tier 3: Advisory (non-blocking)
8. **NPS alignment:** Materials and approach are consistent with what has earned NPS >70 in past engagements.
9. **Methodology contribution:** Reusable frameworks or insights from the engagement are flagged for potential addition to the consulting knowledge base.

## Satisfaction Metric
Target: Client NPS remains >70 across all engagements. If NPS drops below 65 for any engagement, review gate criteria and specific deliverables.

## On Fail
- **Tier 1 failure:** Deliverable cannot go to client. Agent receives specific feedback. Critical: Tier 1 criterion 4 (confidentiality) failure triggers immediate escalation to Natalia + Dan.
- **Tier 2 failure:** Route to Natalia for review with flagged criteria. Natalia decides whether to revise or override.
- **Tier 3 flags:** Informational. Natalia reviews at discretion.

## Escalation Package
When escalated to Natalia, she sees:
- The full deliverable
- Which criteria failed and specific examples
- Client context (industry, maturity level, engagement scope)
- Suggested revisions

## Architecture
- **Type:** Sequential, blocking at Tiers 1-2
- **Runs:** Before any deliverable is shared with a client
- **Natalia's role shift:** Designs engagement quality framework and criteria. Reviews flagged deliverables. Retains final sign-off authority on new engagement types.
- **Brooker Belcourt's role:** Reviews finance-vertical specific deliverables for domain accuracy.

## Political Risk
- **Natalia Quintero (Medium):** Reframed as Knowledge Encoder and Practice Architect. Her methodology scales without diluting. She designs how consulting works at scale. Already proven with Claudie — she welcomes this.
