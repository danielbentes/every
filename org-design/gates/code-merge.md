---
title: "Gate: Code Merge"
layout: default
parent: Quality Gates
nav_order: 2
---

# Gate: Code Merge (Compound Engineering)

## What It Replaces
14-agent parallel code review → GM reviews findings → GM decides to merge. Currently <1 day turnaround. This gate formalizes the already-highly-encoded review process into explicit pass/fail criteria.

## Pass Criteria (visible to executing agent)

### Tier 1: Automated Review (blocking)
1. **All tests pass:** Unit tests, integration tests, linting, type checking — no regressions.
2. **P1 findings resolved:** All Priority 1 findings from review agents (security vulnerabilities, data integrity issues, broken core flows) must be addressed before merge.
3. **Plan adherence:** Implementation follows the approved plan.md or deviations are documented with rationale.
4. **No broken core flows:** End-to-end user journey for the product's primary use case works after the change.

### Tier 2: Compound Quality (blocking)
5. **Compound artifact produced:** At least one of: docs/solutions/ entry, CLAUDE.md update, reusable pattern extracted, or reviewer checklist update. The system must learn from every PR.
6. **Review agent findings triaged:** All P2/P3 findings have been reviewed by GM and either addressed or explicitly deferred with documented rationale.

### Tier 3: Advisory (non-blocking, flags for GM review)
7. **Performance impact:** No measured performance regression beyond acceptable thresholds.
8. **Architecture alignment:** New patterns follow existing codebase conventions (or intentional deviation is documented).
9. **External dependency changes:** Any new dependencies flagged for GM awareness.

## Satisfaction Metric
Target: 95% of PRs passing this gate should ship to production without requiring rollback within 48 hours. If rollback rate exceeds 5%, gate criteria or review agent configuration needs adjustment.

## On Fail
- **Tier 1 failure:** PR cannot merge. Agent receives specific feedback on failing criteria. Agent attempts fix and resubmits.
- **Tier 2 failure:** PR cannot merge. GM is notified with the specific gap (missing compound artifact or unreviewed findings). GM can override if the situation warrants (e.g., hotfix where compound step can be deferred).
- **Tier 3 flags:** Informational only. GM reviews flags at their discretion.
- **Repeated failures (3+ cycles):** Escalate to Engineering Lead (Andrey Galko) to assess whether the plan was insufficient.

## Escalation Package
When escalated, GM sees:
- The full diff
- All review agent findings categorized by priority
- Which specific gate criteria failed
- Agent's self-assessment of the failure
- Suggested fix or explanation of why the agent couldn't resolve it

## Architecture
- **Type:** Sequential (Tier 1 → Tier 2 → Tier 3), blocking at Tiers 1-2
- **Runs:** Before any PR merges to main/production branch
- **Parallel with:** The 14 review agents run in parallel with each other (already standard practice)
- **GM role unchanged:** GMs retain full merge authority. Gate formalizes what they already check; doesn't add new overhead.
- **Override mechanism:** GM can override any Tier 2 failure with documented rationale (e.g., emergency hotfix).

## Political Risk
- **Product GMs (Low):** This gate formalizes their existing workflow, not constraining it. The compound artifact requirement (Tier 2, criterion 5) is new but aligned with compound engineering's core philosophy.
- **Andrey Galko, Engineering Lead (None):** Benefits from formalized quality standards across all GMs.
