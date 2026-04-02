---
title: Self-Review Checklist
layout: default
parent: Compound Engineering
grand_parent: Agents
nav_order: 3
---

# Self-Review Checklist for Compound Engineering Agent

Before requesting GM merge approval, verify against these gates:

### Code Merge Gate (Blocking)
Full criteria: read `gates/code-merge.md`

- [ ] Approved plan exists and was referenced throughout development
- [ ] All deviations from the plan documented with rationale
- [ ] All tests pass (unit, integration, linting, type checking) — zero regressions
- [ ] All 14 review agents completed their analysis
- [ ] All P1 findings resolved (not deferred, not ignored — resolved)
- [ ] All P2/P3 findings triaged with explicit decisions (fix or defer with rationale)
- [ ] Core user flow works end-to-end after the change
- [ ] At least one compound artifact produced (substantive, not token)
- [ ] No user PII collected/stored/transmitted beyond product scope
- [ ] Merge request format complete with all sections
- [ ] Performance assessed — no unacceptable regression
- [ ] New dependencies flagged if applicable
- [ ] Decision logged to decision ledger

## Notes
- Never read `gates/.holdouts/code-merge-holdouts.md`
- Always consult the full gate file before finalizing merge request
