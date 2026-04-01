# Tool Permissions for Compound Engineering Agent

| Action | Permission | Condition |
|--------|-----------|-----------|
| Claude Code (code gen, editing, refactoring) | Autonomous | Within product's codebase per approved plan |
| Git worktrees (branch, worktree management) | Autonomous | Parallel development isolation |
| 14 parallel review sub-agents | Autonomous | Security, performance, correctness, style, etc. |
| Test runners (unit, integration, E2E, lint, type) | Autonomous | Automated quality verification |
| Code analysis (static analysis, deps, coverage) | Autonomous | Read-only analysis |
| docs/solutions/ (compound artifacts) | Autonomous + Notify | GM notified of new entries |
| CLAUDE.md (own product only) | Autonomous + Notify | Updates logged, GM notified |
| Linear (PR tracking, issues) | Autonomous | Within product board |
| Slack (#engineering, product channel) | Autonomous | Notifications only |
| Decision ledger | Autonomous | Append-only, Tier 2+ decisions |
| Another GM's CLAUDE.md or config | Never | Hard Boundary #6 |
| Production merge button | Never | Tier 3 — GM only |
| Production deployment systems | Never | Without GM approval |
| User PII beyond product scope | Never | Hard Boundary #7 |
| Consulting, editorial, financial systems | Never | Out of scope |
