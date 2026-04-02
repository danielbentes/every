---
title: "Authority Matrix (Identity)"
layout: default
parent: Genome
nav_order: 4
---

# Decision Authority Matrix

> This is the organizational decision authority matrix — what gets decided by whom at Every. The `governance/AUTHORITY-MATRIX.md` extends this with agent-type-specific tier assignments (compound engineering, personal, product, consulting, editorial agents), per-tier constraints, and operational detail. Both files are authoritative: this one for organizational identity, governance for agent operations.

## Fully Autonomous (Agent decides, logs, proceeds)

| Decision Type | Examples | Rationale |
|--------------|----------|-----------|
| Bug triage and classification | R2-C2 triaging incoming bug reports, assigning severity | Low-risk, reversible, improves response time |
| Internal task management | Creating Linear tickets, updating status, assigning priority | Pure coordination — no judgment calls on direction |
| Code generation within approved plan | Agent writing code per compound engineering plan | Plan was human-approved; execution is agent domain |
| Research and information gathering | Searching codebase, fetching docs, summarizing findings | Read-only operations with no side effects |
| Draft generation (internal) | Drafting Slack messages, internal docs, CLAUDE.md updates | Internal artifacts; speed > taste |
| File organization (Sparkle) | Organizing user files per learned preferences | Core product function; user has opted in |
| Email triage (Cora) | Categorizing, summarizing, drafting replies for review | Core product function; user reviews before send |
| Test execution | Running test suites, linting, type checking | Automated quality verification |
| Compound engineering review | Running 14 parallel review agents on code changes | Review produces findings; human decides on action |

## Autonomous with Notification (Agent decides, notifies human)

| Decision Type | Examples | Notification To | Rationale |
|--------------|----------|-----------------|-----------|
| Bug auto-fix before review | Agent fixing code flagged by review agents | Product GM | "My AI had already fixed the code before I saw it" — proven workflow |
| Content pipeline nudges | Pinging writers when articles stall past deadline | Managing Editor (Eleanor) | Reduces editorial coordination overhead |
| Client status report generation | Claudie generating weekly consulting client updates | Head of Consulting (Natalia) | Already proven to save 14 hrs/week |
| Social media draft generation | Anthony's Claude+X API system generating post drafts | Social Media Manager (Anthony) | Drafts require human approval before posting |
| Design request routing | Assigning incoming design requests to available designer | Creative Director (Lucas) | Scheduling optimization; human reviews assignments |
| Knowledge base updates | Adding new docs/solutions/ entries from compound loops | Product GM who triggered the loop | Compounding step; human verifies quality of encoding |

## Human-in-Loop (Agent recommends, human approves)

| Decision Type | Examples | Who Approves | Max Wait Time | Default If No Response |
|--------------|----------|-------------|---------------|----------------------|
| Article publication | Final editorial review of article draft | Editor in Chief (Kate Lee) | 48 hours | Hold — never auto-publish |
| Code merge to production | Merging PR after review agents pass | Product GM | 24 hours | Hold — never auto-merge |
| Consulting deliverable delivery | Client-facing materials, training curricula | Head of Consulting (Natalia) | 24 hours | Hold — never auto-deliver |
| Social media posting | Final post content to external platforms | Author + Social Media Manager | 12 hours | Hold — never auto-post |
| Product pricing changes | Any change to subscription/product pricing | CEO (Dan) | No time limit | Hold — never auto-change |
| New consulting engagement scope | Defining engagement terms and deliverables | Head of Consulting + CEO | No time limit | Hold |
| Cross-product data sharing | Sharing user context between products (Cora→Spiral) | User + relevant GMs | No time limit | Deny — data stays siloed |

## Human-Only (Agent surfaces info, human decides and acts)

| Decision Type | Examples | Why Agent Cannot Decide |
|--------------|----------|----------------------|
| Hiring and team changes | Adding team members, role changes, departures | Identity and culture decisions require human judgment about fit |
| Strategic pivots | Narrowing consulting to finance/tech, adopting agent-native architectures | Existential company decisions with irreversible consequences |
| Financial commitments | Pricing, contracts, refunds, investor communications | Legal and fiduciary responsibility |
| Client confidential matters | Access to or sharing of client engagement data | Sacred consulting confidentiality boundary |
| Partnership decisions | Collaborations, sponsorships, co-marketing | Brand and relationship implications require human judgment |
| Editorial direction | Which topics to cover, which writers to recruit, which columns to start/end | Core taste decisions that define Every's identity |
| Investor relations | Fundraising, board communications, financial reporting | Legal and relationship sensitivity |
| Crisis response | Public incidents, security breaches, reputation issues | Requires human judgment, empathy, and accountability |

## Authority Escalation Rules
1. **If unsure which level applies** → treat as one level higher
2. **If time-sensitive and human unavailable** → hold for human (except Fully Autonomous decisions)
3. **If the decision involves external parties** → minimum Human-in-Loop
4. **If the decision involves client data** → Human-Only, always
5. **If the decision could be embarrassing if wrong** → Human-in-Loop minimum
6. **Each GM has full authority within their product domain** — decisions within their product follow GM's personal authority level, not company-wide escalation
