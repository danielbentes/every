---
title: Agent Authority Matrix
layout: default
parent: Governance
nav_order: 1
---

# Agent Decision Authority Matrix

*Every Inc -- Governance v1.0 -- 2026-04-01*

## Design Principles

This matrix extends `genome/01-decision-architecture/AUTHORITY-MATRIX.md` (the organizational decision authority) with agent-type-specific tier assignments, per-tier constraints, and operational detail. The genome version defines *what gets decided by whom* at Every; this version defines *how agents operationalize those decisions*.

It reflects Every's values hierarchy: builder credibility > taste over process > ship and iterate > generalist advantage > play as strategy.

Core premise: **GM autonomy is sacred.** Each product GM has full authority within their product domain. This matrix governs agent behavior within and across those domains, not human authority structures.

---

## Tier 1: Full Autonomy

*Agent decides, logs to decision ledger, proceeds immediately. No human notification required.*

| Decision Type | Agent Types | Examples | Rationale |
|---|---|---|---|
| Bug triage and classification | Compound engineering agents, R2-C2 | Triaging incoming bug reports, assigning severity in Linear, routing to correct GM | Low-risk, reversible, improves response time |
| Code generation within approved plan | Compound engineering work agents | Writing code per a human-approved PRD/plan in the Plan-Work-Review-Compound cycle | Plan was human-approved; execution is agent domain |
| Research and information gathering | All agent types | Searching codebase, fetching docs, summarizing findings, competitive research | Read-only operations with no side effects |
| Internal draft generation | Personal agents (R2-C2, Iris, Montaigne, Margot, Alfredo, Milo) | Drafting Slack messages, internal docs, CLAUDE.md updates for the agent's own human | Internal artifacts -- speed > taste per tradeoff rules |
| File organization | Sparkle | Organizing user files per learned preferences | Core product function; user has opted in |
| Email triage and draft | Cora | Categorizing, summarizing, drafting replies queued for human review | Core product function; user reviews before send |
| Test execution | Compound engineering review agents | Running test suites, linting, type checking, 14-agent parallel code review | Automated quality verification; review produces findings, human decides action |
| Dictation processing | Monologue | Transcribing and structuring voice input | Core product function; no external side effects |
| Writing assistance within session | Spiral | Multi-agent writing loops within a user's active session | User is present and directing; agent assists within session |

### Tier 1 Constraints

- All Tier 1 actions are logged to the decision ledger with timestamp, agent ID, and action type.
- If a Tier 1 action produces an unexpected result (error, anomaly, confidence below threshold), it automatically escalates to Tier 2 (notify) or Tier 3 (human-in-loop) depending on severity.
- No Tier 1 action may produce externally visible output (published content, sent emails, merged code, client communications).

---

## Tier 2: Autonomous + Notify

*Agent decides and acts, then notifies the designated human. Human reviews after the fact and can reverse.*

| Decision Type | Agent Types | Notification Target | Examples | Rationale |
|---|---|---|---|---|
| Bug auto-fix before review | Compound engineering work agents | Product GM (Danny, Yash, Naveen, Kieran) | Fixing code flagged by review agents before GM sees it | Proven workflow -- "my AI had already fixed the code before I saw it" |
| Content pipeline nudges | Editorial AI | Eleanor Warnock (Managing Editor) | Pinging writers when articles stall past deadline, surfacing bottleneck data | Reduces editorial coordination overhead; Eleanor reviews pattern |
| Client status report generation | Claudie | Natalia Quintero (Head of Consulting) | Generating weekly consulting client status updates | Already saves Natalia 14 hrs/week; proven safe at scale |
| Social media draft generation | Anthony's Claude+X API system | Anthony (Social Media) | Generating post drafts based on published articles | Drafts queue for human approval; generation itself is autonomous |
| Knowledge base updates | Compound engineering compounding agents | Product GM who triggered the loop | Adding new docs/solutions/ entries from compound engineering loops | Compounding step; human verifies quality of encoding |
| Design request routing | Personal agents | Lucas Crespo (Creative Director) | Auto-assigning incoming design requests based on capacity and sprint cycles | Scheduling optimization; Lucas reviews assignments |
| AI tells detection flags | Katie Parrott's editorial AI | Kate Lee (EIC) + article author | Flagging formulaic transitions, hedging language, AI-sounding patterns | Detection is autonomous; editorial decision remains human |
| Plus One subscriber agent responses | Plus One (OpenClaw hosted agents) | Relevant GM or support lead | Answering subscriber questions about Every products in Slack | Responses based on approved knowledge base; flagged for review |

### Tier 2 Constraints

- Notifications must be delivered within 5 minutes of action via Slack DM or Linear comment.
- Notification format: `[Agent] [Action taken] [Rationale] [Reversal instructions]`
- If the designated human is unavailable for 24+ hours, pending Tier 2 actions queue for review upon return -- they do not auto-escalate unless a separate escalation trigger fires.
- No Tier 2 action may send communications to external parties (clients, partners, subscribers beyond Plus One's approved scope).

---

## Tier 3: Human-in-Loop

*Agent recommends, human approves before action executes. Agent may prepare everything, but the final gate is human.*

| Decision Type | Agent Types | Approver | Max Wait | Default If No Response |
|---|---|---|---|---|
| Article publication | Editorial AI, personal agents (Margot for Katie) | Kate Lee (EIC) | 48 hours | **Hold** -- never auto-publish |
| Code merge to production | Compound engineering agents | Product GM | 24 hours | **Hold** -- never auto-merge |
| Consulting deliverable delivery | Claudie, personal agents | Natalia Quintero | 24 hours | **Hold** -- never auto-deliver |
| Social media posting | Anthony's Claude+X system | Author + Anthony | 12 hours | **Hold** -- never auto-post |
| Product pricing changes | Any agent | Dan Shipper (CEO) | No time limit | **Hold** -- never auto-change |
| New consulting engagement scope | Claudie | Natalia + Dan | No time limit | **Hold** |
| Cross-product data sharing | Product agents (Cora, Spiral, Sparkle, Monologue) | User + relevant GMs | No time limit | **Deny** -- data stays siloed |
| Podcast episode publication | Production agents | Rachel Braun | 24 hours | **Hold** |
| Email send on behalf of user | Cora | User (in-product confirmation) | No time limit | **Hold** -- draft stays in queue |
| Plus One agent scope expansion | Plus One configuration agents | Relevant GM | No time limit | **Hold** -- agent stays within current scope |

### Tier 3 Constraints

- Agent must present the human with: (1) the proposed action, (2) rationale, (3) alternatives considered, (4) risk assessment, (5) one-click approve/reject.
- **"Hold" means hold.** No Tier 3 action ever auto-executes. If the human never responds, the action never happens.
- The agent may remind the approver once at 50% of max wait time, and once at 90%. After max wait, the agent logs the timeout and stops reminding.
- Builder credibility check: before any customer-facing Tier 3 action, the agent must verify that all claims are grounded in Every's actual experience (per VALUES.md).

---

## Tier 4: Human-Only

*Agent surfaces information and analysis. Human makes the decision AND executes the action. Agent never acts.*

| Decision Type | Examples | Why Agent Cannot Decide |
|---|---|---|
| Hiring and team changes | Adding team members, role changes, departures | Identity and culture decisions require human judgment about fit with Every's generalist model |
| Strategic pivots | Narrowing consulting verticals, adopting new architecture patterns, product launches/kills | Existential decisions with irreversible consequences |
| Financial commitments | Contracts, refunds, investor communications, salary decisions | Legal and fiduciary responsibility; Dan and finance team only |
| Client confidential matters | Access to or sharing of client engagement data across engagements | Sacred consulting confidentiality boundary -- Every's consulting reputation depends on this |
| Partnership decisions | Collaborations, sponsorships, co-marketing, API partnerships | Brand and relationship implications require human judgment |
| Editorial direction | Which topics to cover, which writers to recruit, which columns to start/end | Core taste decisions that define Every's identity -- Kate Lee's domain |
| Investor relations | Fundraising, board communications, financial reporting | Legal and relationship sensitivity; Dan only |
| Crisis response | Public incidents, security breaches, reputation issues | Requires human judgment, empathy, and accountability |
| CLAUDE.md or compound config changes for another GM | Modifying another GM's agent configuration or workflow | GM autonomy is sacred; only the GM themselves modifies their own setup |
| PII handling policy changes | Changes to what user data is collected, stored, or shared | Privacy and compliance decisions require human accountability |

### Tier 4 Constraints

- Agents may prepare analysis, summaries, and options to support human decision-making.
- Agents must never take actions that pre-commit the human (e.g., drafting and sending a contract "for review" to an external party).
- If an agent encounters a situation that maps to Tier 4, it must immediately stop and surface the situation to the appropriate human.

---

## Agent-Type Authority Summary

| Agent Type | Tier 1 | Tier 2 | Tier 3 | Tier 4 |
|---|---|---|---|---|
| **Compound engineering agents** (14 review agents, work agents, planning agents) | Code gen, test execution, research, review | Bug auto-fix, knowledge base updates | Code merge, cross-product data sharing | Strategic architecture decisions |
| **Personal agents** (R2-C2, Iris, Montaigne, Margot, Alfredo, Milo) | Internal drafts, research, task management | Pipeline nudges (if editorial), design routing | Publication, deliverable delivery | Hiring, strategy, finance |
| **Product agents** (Spiral, Cora, Monologue, Sparkle) | Core product function within user session | N/A (product actions are user-initiated) | Email send, cross-product data sharing | Product direction, pricing |
| **Consulting agents** (Claudie, Plus One) | Research, internal status drafts | Client status reports, subscriber responses | Deliverable delivery, engagement scope | Client confidential, contracts |
| **Editorial AI** (Katie's AI tells, Anthony's Claude+X) | AI tells detection, draft generation | Pipeline nudges, social drafts | Publication, social posting | Editorial direction, writer recruitment |

---

## Escalation Rules

1. **If unsure which tier applies** -- treat as one tier higher.
2. **If time-sensitive and human unavailable** -- hold for human (except Tier 1 actions).
3. **If the action involves external parties** -- minimum Tier 3.
4. **If the action involves client data** -- Tier 4, always.
5. **If the action could be embarrassing if wrong** -- minimum Tier 3.
6. **GM autonomy rule**: each GM has full authority within their product domain. Tier assignments within a GM's product follow that GM's personal authority preferences, not this company-wide matrix. This matrix governs cross-domain and company-wide actions.

---

*Reviewed by: Dan Shipper, Brandon Gell*
*Next review: 2026-05-01 (monthly governance review cycle)*
*Governance version: 1.0*
