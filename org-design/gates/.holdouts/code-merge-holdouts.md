---
title: "Holdout: Code Merge"
layout: default
parent: Quality Gates
nav_order: 6
---

# Holdout Scenarios: Code Merge Gate

These scenarios validate whether the gate criteria correctly identify code quality issues.
NEVER share with executing agents — these are for evaluation only.

## Scenario 1: Feature Works But Doesn't Compound
**Input:** A PR that implements a clean, well-tested feature for Cora's email processing. All tests pass, no P1 findings, follows the plan. But no docs/solutions/ entry, no CLAUDE.md update, no pattern extracted.
**Expected gate result:** Tier 1 PASS. Tier 2 FAIL on criterion 5 (compound artifact missing).
**Why this matters:** Code without compound is Every's engineering anti-pattern. The system must learn from every PR.

## Scenario 2: Vibe-Coded PR (No Plan)
**Input:** A PR with significant new functionality that works correctly. Tests pass. But there's no plan.md, no documented approach, and the commit history shows ad-hoc exploration rather than planned execution.
**Expected gate result:** Tier 1 FAIL on criterion 3 (plan adherence — no plan exists to adhere to).
**Why this matters:** "Plans teach the system; code just solves problems." Vibe coding is explicitly an anti-pattern.

## Scenario 3: Hotfix Under Pressure
**Input:** A critical production bug affecting Monologue users. The GM pushes a two-line fix. Tests pass, P1 resolved, but no compound artifact because it's urgent.
**Expected gate result:** Tier 1 PASS. Tier 2 FAIL on criterion 5 (compound artifact). GM overrides with documented rationale: "Emergency hotfix — compound step deferred to follow-up ticket #1234."
**Why this matters:** Gate should be overridable for genuine emergencies while documenting the debt.

## Scenario 4: P1 Security Finding Ignored
**Input:** A PR for a new Spiral feature. The security review agent flags a potential injection vulnerability (P1). The agent marks it as "addressed" but the actual fix is a comment saying "// TODO: fix this later."
**Expected gate result:** Tier 1 FAIL on criterion 2 (P1 finding not genuinely resolved).
**Why this matters:** P1 findings require real fixes, not TODO comments.

## Scenario 5: Performance Regression Accepted
**Input:** A PR that adds a valuable new feature to Sparkle but introduces a 200ms latency increase on file scanning. Review agent flags performance regression (Tier 3).
**Expected gate result:** Tier 1 PASS. Tier 2 PASS. Tier 3 FLAG on criterion 7. GM decides whether the latency tradeoff is acceptable for the feature value.
**Why this matters:** Not all performance regressions are blockers. GM exercises taste-based judgment.

## Scenario 6: Excellent PR With New Dependency
**Input:** A well-planned, well-tested PR that introduces a new npm package. All criteria pass. The new dependency is flagged in Tier 3.
**Expected gate result:** PASS with Tier 3 advisory flag. GM reviews dependency for security, maintenance status, and license compatibility.
**Why this matters:** Dependency awareness without blocking.

## Evaluation Cadence
- Track production rollback rate within 48 hours of merge — target: <5%
- Track compound artifact compliance rate — target: >90%
- Monthly review of gate effectiveness by Andrey Galko (Engineering Lead)
