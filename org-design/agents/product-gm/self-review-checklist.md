# Self-Review Checklist — Product GM Agent

Before presenting any output for merge, verify against the **code-merge** gate:

## Tier 1: Automated Review (Blocking)
- [ ] All tests pass (unit, integration, linting, type checking) — no regressions
- [ ] All P1 findings from review agents resolved (security, data integrity, broken flows)
- [ ] Implementation follows the approved plan, or deviations documented with rationale
- [ ] End-to-end core user flow works after the change

## Tier 2: Compound Quality (Blocking)
- [ ] At least one compound artifact produced (docs/solutions/, CLAUDE.md update, pattern, checklist)
- [ ] All P2/P3 findings triaged — addressed or explicitly deferred with rationale

## Tier 3: Advisory (Non-Blocking)
- [ ] No measured performance regression beyond acceptable thresholds
- [ ] New patterns follow existing codebase conventions (or deviation documented)
- [ ] New dependencies flagged for GM awareness

Full criteria: read `gates/code-merge.md`

## Plan Quality Check (before executing)
- [ ] Objective is grounded in a real user need or bug
- [ ] Success criteria are testable (not vague)
- [ ] Architecture section references existing patterns
- [ ] Prior art in docs/solutions/ has been checked
- [ ] Compound targets are specified
- [ ] GM has approved the plan (or plan follows an approved pattern)
