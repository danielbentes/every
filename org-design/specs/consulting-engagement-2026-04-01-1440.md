---
title: Consulting Engagement
layout: default
parent: Specifications
nav_order: 3
---

# Workflow: Consulting Engagement Delivery

Layer: L2 (Workflow)
Date: 2026-04-01

## Purpose

This workflow produces end-to-end consulting engagements that help finance and tech companies adopt AI effectively — from initial client onboarding through ongoing "Chief AI Officer" support. Every's consulting practice generates $1-2M in revenue and has engaged 100+ companies, with approximately two dozen deep engagements. The core differentiator is builder credibility: Every consultants don't present slides about AI — they show clients what they've built, teach clients to build their own tools, and provide ongoing practitioner support.

Why it matters: Consulting is both a revenue stream and a credibility engine. Every engagement that succeeds reinforces Every's reputation as "the company that practices what it preaches." Every engagement that delivers generic advice or recommends tools Every doesn't use undermines the entire brand — not just the consulting practice, but editorial and product credibility too. Builder credibility is the absolute tiebreaker in Every's value hierarchy, and consulting is where it's tested most directly.

## Trigger

A consulting engagement begins when:
1. An inbound lead arrives (typically through Every's content, podcast, or word-of-mouth referral)
2. Natalia Quintero (Head of Consulting) qualifies the lead against two hard filters:
   - **Vertical fit:** Finance or tech only. Every does not take engagements outside these verticals because builder credibility requires domain-specific practitioner experience.
   - **Engagement fit:** The client's need matches something Every has actually built or practiced internally. If Every can't point to its own experience, the engagement is declined — regardless of revenue.
3. Once qualified, Natalia and the client agree on engagement scope, timeline, and terms

## Steps

### Step 1: Client Onboarding and AI Maturity Assessment
- **Responsible party:** Natalia Quintero + Claudie (AI PM agent)
- **Input:** Signed engagement agreement with scope, timeline, and client contact information
- **Process:**
  1. **AI baseline survey:** Claudie (Natalia's AI project management agent) sends the client a structured assessment that measures their current AI maturity level across four dimensions:
     - **L1 — Awareness:** Team knows AI exists and has experimented individually, but no organizational strategy. Tools used ad hoc. No shared workflows.
     - **L2 — Experimentation:** Some teams actively use AI tools. A few workflows partially automated. Leadership interested but not yet investing systematically.
     - **L3 — Integration:** AI embedded in core workflows. Multiple teams using AI daily. Internal tools and custom agents deployed. Measuring ROI on AI investments.
     - **L4 — Transformation:** AI is a core part of how the organization operates. Human roles have shifted from execution to specification and oversight. Institutional knowledge is encoded into agent systems.
  2. **Onboarding data collection:** Claudie gathers: team size, department structure, current AI tools in use, top 3-5 workflows the client wants to improve, technical infrastructure, data sensitivity constraints, and key stakeholders.
  3. **Maturity classification:** Based on survey responses, Natalia classifies the client at L1-L4 and identifies the target maturity level for the engagement. Most clients are L1-L2 targeting L2-L3.
  4. **Engagement plan creation:** Natalia produces a tailored engagement plan specifying: which phases apply, timeline per phase, deliverables, success metrics, and Every team members involved.
- **Output:** Client maturity assessment (L1-L4), engagement plan, and onboarding package
- **Criteria for completion:** Client maturity level confirmed, engagement plan reviewed and approved by client, all onboarding data collected
- **Time budget:** 1-2 weeks
- **Claudie's role:** Claudie handles the mechanics — sending surveys, collecting responses, generating initial maturity classification drafts, producing weekly status updates. Natalia makes all classification and strategy decisions. Claudie saves approximately 14 hours/week on these logistics.

### Step 2: Workflow Building (Custom Tools and Agents)
- **Responsible party:** Natalia + relevant Every team members (Brooker Belcourt for finance-vertical depth, other specialists as needed)
- **Input:** Engagement plan, client maturity assessment, identified workflows to improve
- **Process:**
  1. **Workflow audit:** For each client workflow targeted for improvement, map the current state: who does what, how long it takes, where are the bottlenecks, what's manual that shouldn't be.
  2. **Solution design:** Design AI-assisted workflows grounded in Every's own experience. For each proposed solution:
     - Reference how Every does something similar internally. Example: "We use compound engineering to ship features with a single GM. Here's how we adapted a similar approach for [another client in your vertical]."
     - If no direct Every parallel exists, be transparent: "We haven't done exactly this, but here's the closest analog from our experience, and here's how we'd adapt it."
  3. **Tool and agent building:** Build custom tools, agents, or workflows tailored to the client's specific environment. This is hands-on building, not recommendations on paper. Common deliverables:
     - Custom Claude Skills or system prompts for client-specific tasks
     - Workflow automation using the client's existing tools + AI integration
     - Internal AI agents (similar to Every's Claudie, R2-C2, etc.)
     - Quality gates and review systems adapted from Every's own gate architecture
  4. **Builder credibility checkpoint:** Before delivering any solution, verify: "Have we used something like this ourselves? Can we honestly say 'We built this, here's what we learned'?" If the answer is no, redesign or scope down.
- **Output:** Working tools/agents/workflows deployed in the client's environment, with documentation
- **Criteria for completion:** Each target workflow has a working AI-assisted version that the client has seen demonstrated. Solutions reference Every's actual practice.
- **Time budget:** 2-6 weeks depending on number and complexity of workflows

### Step 3: Training (Department-Specific)
- **Responsible party:** Natalia + relevant Every team members
- **Input:** Built tools/agents/workflows from Step 2, client team roster by department
- **Process:**
  1. **Department-specific sessions:** Training is customized per department. An engineering team gets different training than a marketing team, even within the same client. Each session covers:
     - The specific tools and workflows built for that department
     - Hands-on building exercises — participants build or extend something during the session, not just watch a demo
     - Common pitfalls and how to avoid them (drawn from Every's own experience)
     - How to evaluate AI output quality (adapted from Every's quality standards)
  2. **Builder credibility in training:** Trainers demonstrate by doing, not by presenting. "Let me show you how I use this" not "Here's a slide about best practices." Every trainer must have personal experience with the tools being taught.
  3. **Hands-on component requirement:** Every training session must include at least 30 minutes of participants building something themselves. No session is all-lecture.
  4. **NPS measurement:** After each training session, collect Net Promoter Score from participants. Target: NPS >70.
  5. **Follow-up resources:** Provide each participant with: quick-reference guide for their new tools, contact for questions, and a 30-day check-in schedule.
- **Output:** Trained client teams, session recordings, reference materials, NPS scores
- **Criteria for completion:** All target departments trained. NPS collected for each session. NPS >70 target met (if below, escalate to Natalia for remediation plan).
- **Time budget:** 1-3 weeks depending on number of departments

### Step 4: Ongoing Support (Chief AI Officer Role)
- **Responsible party:** Natalia (strategic), Claudie (operational)
- **Input:** Completed training, deployed tools/workflows, client relationship
- **Process:**
  1. **Weekly status updates:** Claudie generates and sends weekly status updates to the client covering: adoption metrics (who's using the tools, how often), issues reported, upcoming milestones, and any new AI developments relevant to the client's workflows.
  2. **Monthly strategy calls:** Natalia conducts monthly calls with client leadership to review:
     - Progress against the engagement's success metrics
     - New workflow opportunities identified since training
     - Organizational changes that affect AI adoption (new hires, team restructuring, etc.)
     - Whether the client's maturity level has shifted (L1→L2, L2→L3, etc.)
  3. **Issue resolution:** When client teams encounter problems with deployed tools, they contact Every through a dedicated Slack channel or email. Claudie triages incoming requests: technical issues routed to resolution, strategic questions flagged for Natalia.
  4. **Maturity advancement:** As the client advances in AI maturity, adjust support accordingly. L1→L2 clients need more hand-holding. L3→L4 clients need more strategic guidance and less operational support.
  5. **Engagement renewal/expansion:** Based on client progress and satisfaction, Natalia proposes next-phase work: new departments, deeper integrations, advanced agent architectures. Renewal discussions happen during monthly strategy calls.
- **Output:** Ongoing client support, adoption metrics, maturity progression tracking, engagement renewal proposals
- **Criteria for completion:** This phase continues for the duration of the engagement agreement. Phase-end criteria: client has achieved the target maturity level specified in the engagement plan, or the engagement is formally concluded with a summary report.

## Execution Model

- **Sequential dependencies:** Step 1 (Onboarding) → Step 2 (Workflow Building) → Step 3 (Training) → Step 4 (Ongoing Support). Steps 2-3 may iterate (build a workflow, train on it, build the next).
- **Parallel stages:** Within Step 2, multiple workflows can be built concurrently if they don't depend on each other. Claudie handles logistics (status reports, scheduling) in parallel with all substantive work.
- **Convergence point:** Step 3 (Training) — where built tools meet the client team. Training sessions test whether the tools are usable and the workflows are practical. If training reveals the workflow doesn't work as designed, loop back to Step 2.
- **Blocking gate:** Consulting Deliverable Gate before any client-facing material is delivered.
- **Client variation:** L1 clients need more training (Step 3 emphasis). L3-L4 clients need more building (Step 2 emphasis). The sequence is the same; the time allocation shifts.

## Feedback Loops

- **Training NPS → Curriculum:** Post-training NPS (target >70) feeds back into curriculum design. Sessions scoring below 70 are analyzed: was it the content, the delivery, or the tool?
- **Client Outcomes → Methodology:** When a client workflow produces measurable results (hours saved, processes automated), the approach is generalized into Every's consulting knowledge base.
- **Claudie → Claudie:** Natalia's AI PM agent learns from each engagement. Onboarding templates, status report formats, and scheduling patterns improve with each client cycle.
- **Engagement Results → Articles:** Successful client outcomes become source material for Every's articles and case studies (with client permission), completing the business flywheel: consulting → content → distribution → more consulting leads.

## Quality Gate

**[Consulting Deliverable Gate]({% link org-design/gates/consulting-deliverable.md %})**

Applied before any deliverable is shared with a client — including strategy assessments, built tools, training materials, and status reports.

- **Tier 1 (blocking — builder credibility):** Every recommendation references Every's actual experience. No unfamiliar tools recommended. No overselling. Client confidentiality protected.
- **Tier 2 (blocking — quality):** Materials are customized to client's vertical, size, and maturity level. At least one recommendation is implementable within the client's first week. Includes hands-on component.
- **Tier 3 (advisory):** NPS alignment, methodology contribution flagged.

**Hard boundary on Tier 1, Criterion 4 (confidentiality):** Any confidentiality failure triggers immediate escalation to Natalia + Dan Shipper (CEO). This is a zero-tolerance boundary.

## Stranger Test

**Could someone with zero context execute this workflow from this spec alone?**

Partially. The steps are clear and the quality criteria are explicit, but consulting requires domain expertise that can't be fully encoded:

1. **Vertical expertise:** A stranger would need deep familiarity with either finance or tech industries to deliver credible consulting. Every only takes engagements in these verticals because the team has practitioner experience there. A new consultant would need to shadow Natalia on 2-3 engagements before leading one independently.

2. **Claudie access and configuration:** Claudie is Natalia's custom-built AI PM agent. A new team member needs Claudie access, training on how to use it, and understanding of its capabilities and limitations. Natalia is the authority here.

3. **Every's internal reference library:** Step 2 requires referencing "how Every does this internally." A new consultant needs to know Every's products, tools, and workflows well enough to draw these parallels authentically. Minimum onboarding: 2 weeks using Every's products and reading the organizational genome.

4. **Builder credibility verification:** The checkpoint in Step 2 ("Have we used something like this ourselves?") requires knowing what Every has and hasn't built. The genome, audit, and team knowledge base provide this context, but a new consultant should verify with Natalia before making claims about Every's experience.

5. **Client relationship management:** Monthly strategy calls (Step 4) require the ability to read organizational dynamics, suggest without overselling, and maintain trust over time. This is a human skill that develops with experience.

6. **Brooker Belcourt's finance expertise:** Finance-vertical engagements require domain-specific review from Brooker. A stranger would need to know when to loop him in (any finance-specific deliverable).

**Verdict:** A competent consultant with AI expertise and either finance or tech domain knowledge could follow this spec after a 2-3 week onboarding period that includes shadowing existing engagements and learning Every's internal tools. The spec is explicit about what to deliver and how to quality-check it; the gap is the domain knowledge and relationship skills that come with practice.

## Iteration Protocol

This workflow improves through the following mechanisms:

1. **NPS tracking and analysis:** Every training session produces an NPS score. Scores are tracked per department type, client vertical, maturity level, and trainer. Patterns emerge: "Finance L2 clients rate workflow-building sessions higher when we include live trading-floor examples." These patterns become explicit guidance for future engagements.

2. **Engagement retrospectives:** At the conclusion of each engagement (or each phase), Natalia conducts a retrospective: What worked? What didn't? What would we do differently? Key findings are documented in the consulting knowledge base.

3. **Maturity framework refinement:** As more clients are assessed, the L1-L4 framework becomes more precise. Observable behaviors at each level become more clearly defined. Assessment questions are refined based on what actually predicts a client's readiness for the next level.

4. **Claudie capability expansion:** Each engagement teaches Claudie new patterns. New status report templates, new survey questions, new triage rules — Natalia evolves Claudie's capabilities based on what she learns from each client.

5. **Cross-engagement pattern library:** When a solution built for one client applies to another (respecting confidentiality), the pattern is extracted into a reusable template. Over time, common consulting deliverables become faster to produce because templates exist for common client profiles.

6. **Builder credibility log:** Maintain a running list of "things we've actually built and can reference in consulting." When Every's products or internal tools evolve, update this log. When a consulting engagement requires something not on the list, flag it as a potential internal project — this is how consulting needs feed back into product development.
