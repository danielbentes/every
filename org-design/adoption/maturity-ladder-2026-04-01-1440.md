---
title: Maturity Ladder
layout: default
parent: Adoption
nav_order: 1
---

# AI Adoption Maturity Ladder — Every Inc.
Date: 2026-04-01

## Maturity Model Definition

| Level | Label | Observable Threshold | Mindset |
|-------|-------|---------------------|---------|
| 0 | Not Engaged | No AI-assisted work tasks in past 30 days | "I do my job without AI" |
| 1 | Capable | Uses AI for 3+ distinct tasks/week, reviews all output, follows usage policy | "AI is a useful tool" |
| 2 | Adoptive | Has designed at least 1 reusable AI workflow, delegates execution to AI by default | "I specify, AI executes" |
| 3 | Transformative | Has built or extended an AI tool/skill/workflow that others now use | "I create new capabilities" |

---

## Organization Summary

**Company:** Every Inc. (~20 people)
**Assessment date:** 2026-04-01
**Assessor context:** Coordination audit data, VALUES.md, published behavioral evidence

### Distribution

| Level | Count | % of Team |
|-------|-------|-----------|
| 3 — Transformative | 9 | 47% |
| 2 — Adoptive | 7 | 37% |
| 1-2 — Transitional | 2 | 11% |
| 1 — Capable | 1 | 5% |
| 0 — Not Engaged | 0 | 0% |

**Organizational mean: 2.4** — Exceptionally high for a 20-person company. No one is at Level 0. The floor is Level 1. Every's "builder credibility" value and GM autonomy model create structural pressure toward Level 3.

---

## Per-Role Maturity Assessments

### 1. Dan Shipper — CEO

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Built Proof, an agent-native document editor used by the entire team and consulting clients
- Created R2-C2, a personal agent that others reference as a model
- Co-architected the compound engineering framework (12K+ GitHub stars, used by all GMs)
- Pioneered AI journaling practices documented in published articles
- Writes extensively about AI adoption from practitioner experience, embodying builder credibility

**Primary Barrier:** None at this level. Risk is *overextension* — CEO time split across building, writing, fundraising, and managing. The barrier is not adoption but allocation.

**Progression Path:** Dan is at the ceiling of the individual model. His next frontier is *organizational multiplication* — ensuring his Level 3 practices propagate systematically rather than through osmosis. This means shifting from "Dan builds tools others use" to "Dan builds systems that help others build tools."

**Role-Specific Level Definitions:**
- Level 2 (CEO): Uses AI agents for personal productivity (writing, scheduling, analysis), delegates routine CEO tasks to AI
- Level 3 (CEO): Builds AI tools/frameworks adopted company-wide, shapes product strategy around AI-native principles, serves as credible external practitioner voice

---

### 2. Brandon Gell — CTO

**Current Level: 2, trending toward 3**

**Observable Evidence:**
- Built Milo, a personal agent for operational work
- Builds operational systems infrastructure
- Manages technical architecture across 4 products
- Adopted "be sincere, not serious" mantra that shapes engineering culture

**Primary Barrier:** *Authority distribution.* As CTO of a company where each GM owns their full stack, Brandon's role is more infrastructure and culture than direct technical authority. Building tools that GMs voluntarily adopt (vs. mandating) is the Level 3 challenge for this specific role.

**Progression Path:** Build or extend a shared operational tool/system that multiple GMs adopt organically. Candidates: extending the 14-agent code review system, building shared infrastructure tooling, or creating a cross-product technical standards system that GMs choose to use.

**Role-Specific Level Definitions:**
- Level 2 (CTO): Personal agent usage, delegates operational tasks to AI, manages AI infrastructure
- Level 3 (CTO): Builds shared engineering tools/systems adopted across all products, shapes the technical environment that enables compound engineering at scale

---

### 3. Kate Lee — Editor-in-Chief

**Current Level: 2, trending toward 3**

**Observable Evidence:**
- Created the three rigor tests (articulates something true, offers learnable value, sounds authentically like the writer) that define Every's editorial quality bar
- Uses Katie Parrott's AI tells detection output as input to her editorial review workflow
- Applies editorial taste judgment on top of AI-assisted pipeline
- Key bottleneck in article production pipeline (audit: editorial review is throughput constraint)

**Primary Barrier:** *Identity threat (mild).* Kate's value is taste — "the ability to recognize quality, requiring knowledge plus intuition." AI tells detection is Level 2 because it's a reusable workflow. The path to Level 3 requires building editorial tools that *encode* taste without threatening the editorial identity that taste is irreducibly human. This is a real tension, not resistance — it's the correct instinct to protect the cultural function of editorial judgment.

**Progression Path:** Build a shareable editorial quality gate — a specification or tool that other editors (including freelancers and the 40 contributing writers) can use to self-check against Every's rigor tests before submission. This would reduce the bottleneck while preserving Kate's final judgment authority. The key framing: "I'm not automating my taste, I'm scaling my standards."

**Role-Specific Level Definitions:**
- Level 2 (EIC): Reusable AI workflows for editorial tasks (AI tells detection, first-pass review), delegates mechanical editorial tasks to AI
- Level 3 (EIC): Builds editorial quality tools/specifications used by all writers and editors, encodes quality standards into shareable systems while preserving human taste authority

---

### 4. Eleanor Warnock — Managing Editor

**Current Level: 1, trending toward 2**

**Observable Evidence:**
- Uses AI for first-pass triage of incoming articles
- Uses AI for technical accessibility editing (making complex topics readable)
- Part of the editorial review bottleneck identified in audit
- No evidence of reusable workflow design or tool building yet

**Primary Barrier:** *Opacity + Identity threat.* Managing editors traditionally derive authority from being the throughput engine — knowing every piece's status, managing the pipeline, being the person who "keeps the trains running." AI that automates pipeline management can feel like it removes the role's core value proposition. Additionally, editorial judgment in accessibility editing is hard to specify — it requires understanding what a non-technical reader will find confusing, which is opaque to articulate as an AI workflow.

**Progression Path:** Design a reusable AI workflow for one of: (a) article pipeline triage — structured intake that auto-categorizes, estimates editorial effort, and flags bottleneck risks, or (b) accessibility editing — a prompt chain that identifies jargon, assumes-too-much passages, and unclear analogies in technical drafts. Either would be a clear Level 2 artifact. The audit's "Editorial Pipeline Management" encoding candidate (25 hrs/month, 70/30 coordination/cultural split) is the natural target.

**Role-Specific Level Definitions:**
- Level 2 (Managing Editor): Has built at least 1 reusable editorial workflow (pipeline triage, accessibility checking, scheduling automation), delegates pipeline logistics to AI by default
- Level 3 (Managing Editor): Built editorial pipeline tools used by the full writing team, automated coordination that frees editorial time for taste work

---

### 5. Katie Parrott — AI Editorial Lead

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Coined "AI-native writing is sculpture" — a conceptual framework others now reference
- Built custom AI tells detection skills used in the editorial pipeline
- Her detection skills are part of the production workflow used by Kate and Eleanor
- Defines the boundary between AI-acceptable and AI-problematic writing for the entire organization

**Primary Barrier:** None. Katie has crossed the Level 3 threshold cleanly. Her next challenge is *maintaining the edge* — as AI writing improves, the detection methodology must evolve continuously.

**Progression Path:** Extend detection skills into a publishable framework or tool that consulting clients and external writers can use. This aligns with Every's builder credibility value and could become a consulting product.

**Role-Specific Level Definitions:**
- Level 2 (AI Editorial Lead): Reusable AI detection workflows, delegates first-pass detection to AI
- Level 3 (AI Editorial Lead): Detection skills used org-wide and potentially externally, shapes the company's definition of AI-native writing quality

---

### 6. Kieran Klaassen — GM, Cora

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Invented the compound engineering methodology now used by all GMs (12K+ GitHub stars)
- Runs 4-5 parallel Claude instances simultaneously
- Plan-first approach to compound engineering that others have adopted
- Built and maintains Cora as solo GM

**Primary Barrier:** None. Kieran is the archetype of Level 3 at Every — he built the methodology that defines how the company builds software.

**Progression Path:** Already at ceiling. Frontier is *methodology evolution* — extending compound engineering for multi-agent orchestration, or building tooling that makes the methodology accessible to non-Every engineers (consulting reach).

**Role-Specific Level Definitions:**
- Level 2 (GM): Uses AI agents for all execution, has personal compound engineering workflow, delegates code production entirely to AI
- Level 3 (GM): Built tools, methodologies, or workflows adopted by other GMs or the broader community, shapes how compound engineering evolves

---

### 7. Naveen Naidu — GM, Monologue

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Manages a 143K-line codebase solo — extraordinary for a single engineer
- Linear-centric workflow that integrates AI throughout the product development cycle
- Uses Codex specifically for brainstorming, showing deliberate tool-task matching
- Runs entire product: strategy, engineering, design direction, metrics, customer support, marketing

**Primary Barrier:** None. The 143K-line solo codebase is definitive Level 3 evidence — it's only possible because of transformative AI integration.

**Progression Path:** Document and share the Linear-centric workflow as a reusable pattern for other GMs. The audit identified "Cross-GM Knowledge Transfer" (20 hrs/month lost to reinvention) as an encoding candidate — Naveen's workflow documentation could directly address this.

**Role-Specific Level Definitions:**
- Level 2 (GM): See Kieran above
- Level 3 (GM): See Kieran above

---

### 8. Yash Poojary — GM, Sparkle

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Runs parallel Claude + Codex sessions for different task types
- Built AgentWatch — a tool for monitoring agent activity (used by others)
- Writes a learnings document after each push — systematic compounding behavior
- Deliberate multi-tool strategy (not just using one AI tool for everything)

**Primary Barrier:** None. AgentWatch is definitive Level 3 — he built a tool that others now use.

**Progression Path:** AgentWatch could become a product or shared infrastructure component. The learnings-after-each-push practice is a compounding discipline that could be formalized into a team-wide standard.

**Role-Specific Level Definitions:**
- Level 2 (GM): See Kieran above
- Level 3 (GM): See Kieran above

---

### 9. Danny Aziz — GM, Spiral

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Built Droid, a custom CLI that handles 70% of his workflow
- Built Spiral v3 solo using Claude Code
- Abandoned Cursor entirely — made a deliberate tool migration based on productivity evidence
- The willingness to abandon a tool (Cursor) that works for one that works better is strong Level 3 signal

**Primary Barrier:** None. Droid is definitive Level 3 — a custom tool built from scratch that transforms his own workflow. Abandoning Cursor shows tool-critical thinking, not just tool adoption.

**Progression Path:** Droid CLI could be generalized for other GMs or open-sourced. Danny's radical tool evaluation practice (abandon what doesn't work, build what you need) could be documented as a decision framework.

**Role-Specific Level Definitions:**
- Level 2 (GM): See Kieran above
- Level 3 (GM): See Kieran above

---

### 10. Andrey Galko — Engineering Lead

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Values simplicity in engineering approaches
- Made deliberate switch from Cursor to Codex — shows tool evaluation behavior
- Supports engineering infrastructure across products

**Primary Barrier:** *Self-enhancing bias (mild).* Andrey values simplicity, which is a strength — but it may create a preference for using AI tools as-is rather than building custom extensions. The "simplicity" value and "build custom tools" impulse can feel contradictory. The reframe: the simplest solution is often a custom tool that eliminates complexity elsewhere.

**Progression Path:** Build or extend a shared engineering tool — a simplified deployment pipeline, a cross-product testing framework, or an extension to the 14-agent code review system. The tool should embody Andrey's simplicity value while being useful to multiple GMs.

**Role-Specific Level Definitions:**
- Level 2 (Engineering Lead): Reusable AI workflows for engineering tasks, delegates execution to AI tools, makes deliberate tool choices
- Level 3 (Engineering Lead): Builds shared engineering infrastructure or tools used across products, shapes the team's engineering tooling standards

---

### 11. Nityesh Agarwal — Engineer, Cora

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Uses Claude Code exclusively — committed to a single AI development environment
- Does detailed pre-research before engaging AI — disciplined specification behavior
- Works within Kieran's compound engineering methodology on Cora

**Primary Barrier:** *Self-enhancing bias (mild).* Nityesh's detailed pre-research approach is excellent specification behavior (Level 2), but may create a pattern where the human always does the research and the AI always does the execution. Level 3 requires building something that changes the workflow itself.

**Progression Path:** Build a reusable tool or workflow extension — a pre-research template that other engineers can use, an extension to Claude Code's workflow for Cora-specific patterns, or a documentation system that auto-captures the research-to-implementation chain. Working closely with Kieran on Cora provides natural mentorship toward Level 3.

**Role-Specific Level Definitions:**
- Level 2 (Engineer): Uses AI for all execution with disciplined specification, has personal AI workflow
- Level 3 (Engineer): Builds tools, extensions, or workflow patterns adopted by other engineers

---

### 12. Natalia Quintero — Head of Consulting

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Built Claudie, an AI project manager agent that saves 14 hours/week
- Claudie is referenced in the audit as a proven system worth extending to all consulting engagements
- Uses compound engineering methodology in client-facing consulting work
- Bridges internal practice and external consulting — ultimate builder credibility

**Primary Barrier:** None. Claudie is definitive Level 3 — a tool she built that the audit recommends scaling across the organization.

**Progression Path:** Scale Claudie beyond personal use to all consulting engagements (audit Quick Win #2). Develop a consulting-specific compound engineering playbook that new consulting team members or contract consultants can use. Claudie's architecture could become a template for role-specific AI agents across Every.

**Role-Specific Level Definitions:**
- Level 2 (Head of Consulting): Reusable AI workflows for consulting delivery, delegates routine client logistics to AI
- Level 3 (Head of Consulting): Built AI tools used across the consulting practice and referenced as client examples, shapes how Every delivers consulting through AI

---

### 13. Brooker Belcourt — Finance Lead

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Uses compound engineering methodology for finance consulting with clients
- Applies AI in finance workflows
- Bridges internal finance function and external consulting

**Primary Barrier:** *Opacity.* Finance workflows involve sensitive data, regulatory considerations, and precision requirements that make AI delegation feel risky. The barrier is not resistance but legitimate caution — financial errors have outsized consequences. The challenge is building AI workflows that maintain auditability and accuracy guarantees.

**Progression Path:** Build a reusable finance analysis workflow with built-in verification steps — an AI-assisted financial modeling tool, an automated reporting pipeline with human checkpoints, or a client-facing finance analysis template. The key is encoding the verification logic so AI handles throughput while maintaining financial accuracy standards.

**Role-Specific Level Definitions:**
- Level 2 (Finance Lead): Reusable AI workflows for financial analysis and reporting, delegates routine finance tasks to AI with verification
- Level 3 (Finance Lead): Builds finance-specific AI tools or templates used by consulting clients, creates auditable AI workflows that others trust for financial decisions

---

### 14. Lucas Crespo — Creative Director

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Built Alfredo, a personal AI agent
- Integrated Figma MCP into design workflow — connects AI to the core design tool
- Leads 3-person design team that rotates across 4 products + consulting + marketing

**Primary Barrier:** *Identity threat (moderate).* Design is a discipline where "taste" and "human judgment" are deeply tied to professional identity. The Figma MCP integration is Level 2 — it delegates execution. Level 3 requires building tools that shape how design is done, which can feel like automating the judgment that makes a designer valuable. Every's "taste over process" value reinforces this tension — it explicitly values human taste over systematic processes.

**Progression Path:** Build a design system tool that helps the 3-person team context-switch efficiently across 4 products. The audit identified "Design Request Intake & Scheduling" (40 hrs/month, 80/20 coordination/cultural split) as the top encoding candidate. Lucas could build this system — a structured intake + auto-scheduling tool that reduces the 40 hrs/month coordination overhead while keeping design critique meetings human. This reframes AI as *protecting* design time rather than replacing design judgment.

**Role-Specific Level Definitions:**
- Level 2 (Creative Director): Personal AI agent, AI-integrated design tools (Figma MCP), delegates production tasks to AI
- Level 3 (Creative Director): Builds shared design system tools used across products, creates AI-assisted design workflows that the full team adopts

---

### 15. Austin Tedesco — Head of Growth

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Built Montaigne, a personal AI agent for growth work
- Uses Proof for campaign strategy development
- Applies AI across growth functions

**Primary Barrier:** *Self-enhancing bias (mild).* Growth work is highly measurable — attribution, conversion rates, CAC. It's tempting to use AI as an efficiency tool (write more copy, test more variants) rather than building systems that transform how growth is done. The barrier is using AI at the task level rather than the system level.

**Progression Path:** Build a growth experimentation system — an AI-assisted pipeline that generates hypotheses, creates test variants, monitors results, and compounds learnings across campaigns. This would transform growth from "use AI to write ads" to "AI runs the growth experimentation loop." The Montaigne agent could evolve into this system.

**Role-Specific Level Definitions:**
- Level 2 (Head of Growth): Personal AI agent, uses AI for campaign creation and analysis, delegates growth execution tasks to AI
- Level 3 (Head of Growth): Builds growth systems or tools used across the company or by consulting clients, creates AI-native growth methodologies

---

### 16. Anukshi Mittal — Product Marketing

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Built Iris, a personal AI agent
- Applies AI in product marketing workflows

**Primary Barrier:** *Self-enhancing bias (mild).* Similar to growth — marketing AI usage can plateau at "generates drafts faster" without reaching "transforms how marketing is structured." The personal agent (Iris) shows Level 2 delegation behavior.

**Progression Path:** Build a product marketing tool or workflow used by others — a launch playbook system, a competitive analysis pipeline, or a messaging framework generator that consulting clients or other team members adopt. The path from "Iris helps me" to "Iris (or a derivative) helps the team" is the Level 3 bridge.

**Role-Specific Level Definitions:**
- Level 2 (Product Marketing): Personal AI agent, reusable AI workflows for marketing tasks, delegates content creation to AI
- Level 3 (Product Marketing): Builds marketing tools or frameworks adopted across the company or by consulting clients

---

### 17. Rachel Braun — Podcast Producer

**Current Level: 2 (Adoptive)**

**Observable Evidence:**
- Uses Descript for AI-assisted post-production
- Uses StreamYard with AI features for recording
- Manages the most execution-heavy workflow at Every (audit: 45% execution)

**Primary Barrier:** *Opacity.* Podcast production has high execution density — recording, editing, post-production are inherently sequential and partially physical (microphones, guest coordination). The audit shows this workflow at 30% specification / 25% coordination / 45% execution — the most execution-heavy at Every. The AI frontier in audio/video is moving fast but is less mature than text-based AI. The barrier is that the tools for Level 3 podcast production may not fully exist yet.

**Progression Path:** Build a podcast production pipeline tool — automated show notes generation, AI-assisted episode planning, an automated distribution workflow that others could use. The audit's "Podcast Production Logistics" encoding candidate (15 hrs/month, 80/20 coordination/cultural split) is the natural target. Alternatively, develop a reusable AI-assisted guest research and prep system.

**Role-Specific Level Definitions:**
- Level 2 (Podcast Producer): Uses AI tools (Descript, StreamYard) for production, delegates post-production and distribution tasks to AI
- Level 3 (Podcast Producer): Builds podcast production tools or workflows adopted beyond personal use, creates AI-native production pipelines

---

### 18. Anthony Scarpulla — Social Media

**Current Level: 3 (Transformative)**

**Observable Evidence:**
- Built a custom Claude Code + X (Twitter) API integration
- This is a purpose-built tool, not just using existing AI features
- Connects AI directly to distribution channels for social media management

**Primary Barrier:** None. Building a custom API integration is definitive Level 3 — it's a tool that transforms the workflow rather than assisting within existing tools.

**Progression Path:** Extend the Claude Code + X integration into a multi-platform social distribution system. Could become a shared tool for the growth team or a consulting deliverable example.

**Role-Specific Level Definitions:**
- Level 2 (Social Media): Reusable AI workflows for content creation, scheduling, and analytics, delegates routine social tasks to AI
- Level 3 (Social Media): Builds custom AI tools for social distribution used beyond personal workflow, creates AI-native social media systems

---

### 19. Jack Cheng — Contributing Editor

**Current Level: 1, trending toward 2**

**Observable Evidence:**
- Uses AI to assist writing
- Contributing editor role (not full-time) limits exposure to Every's internal AI practices
- No evidence of reusable workflow design or tool building

**Primary Barrier:** *Identity threat + Opacity.* Writers have the strongest identity-threat response to AI — "writing is thinking" and "AI writing is not real writing" are deeply held beliefs in the writing profession. For a contributing editor, the barrier is compounded by limited immersion in Every's AI-native culture. The opacity barrier is real too: it's hard to articulate what makes good writing good, which makes it hard to specify AI writing workflows.

**Progression Path:** Design one reusable AI-assisted writing workflow — a research synthesis pipeline, a structural editing checklist, or a revision workflow that uses AI for specific, bounded tasks while preserving the writer's voice and judgment. Katie Parrott's "AI-native writing is sculpture" framing is the right mental model — the writer shapes, AI provides material. A buddy pairing with Katie for one article cycle would accelerate this transition.

**Role-Specific Level Definitions:**
- Level 2 (Contributing Editor): Has at least 1 reusable AI writing workflow, delegates research/structural tasks to AI by default while maintaining voice authority
- Level 3 (Contributing Editor): Develops AI-native writing techniques or tools adopted by other writers at Every

---

## Barrier Analysis Summary

| Barrier Type | Definition | Affected Roles | Prevalence |
|-------------|-----------|----------------|------------|
| Self-enhancing bias | "AI makes me faster at my current tasks" — plateau at efficiency gains without workflow transformation | Austin, Anukshi, Andrey, Nityesh | 4/19 (21%) |
| Identity threat | "AI threatens what makes my role valuable" — resistance to encoding professional judgment | Kate (mild), Lucas (moderate), Eleanor (mild), Jack (moderate) | 4/19 (21%) |
| Opacity | "I can't articulate my expertise well enough to specify it for AI" — difficulty encoding tacit knowledge | Eleanor, Brooker, Rachel, Jack | 4/19 (21%) |
| Authority threat | "AI reduces my organizational influence" — concern about losing decision authority | None detected | 0/19 (0%) |

**Notable finding:** Zero authority-threat barriers detected. This is remarkable and likely attributable to Every's flat GM autonomy model — there are almost no hierarchical authority structures for AI to threaten. The "two-slice team" structure means authority comes from ownership, not position, and AI amplifies ownership rather than undermining it.

---

## Progression Priority Matrix

### Highest ROI Progressions (Level 2 to 3)

These individuals are closest to Level 3 and their progression would have outsized organizational impact:

| Person | Current | Target | Organizational Impact | Recommended Action |
|--------|---------|--------|----------------------|-------------------|
| Kate Lee | 2→3 | 3 | Unblocks editorial pipeline bottleneck (audit finding) | Build shareable editorial quality gate for writers |
| Brandon Gell | 2→3 | 3 | Improves cross-product engineering infrastructure | Build shared operational tool adopted by GMs |
| Lucas Crespo | 2→3 | 3 | Reduces 40 hrs/month design coordination overhead (audit #1 candidate) | Build design request intake system |
| Brooker Belcourt | 2→3 | 3 | Strengthens finance consulting credibility and capacity | Build auditable finance AI workflow |

### Critical Floor-Raising (Level 1 to 2)

| Person | Current | Target | Recommended Action |
|--------|---------|--------|-------------------|
| Eleanor Warnock | 1→2 | 2 | Design one reusable editorial pipeline workflow; pair with Katie Parrott |
| Jack Cheng | 1→2 | 2 | Design one reusable AI writing workflow; buddy with Katie Parrott for one article cycle |

---

## Visibility Infrastructure

How Every currently makes AI adoption visible — and recommendations for strengthening it.

### Current Visibility Mechanisms

**1. Weekly All-Hands / Demo Day**
- *Function:* Team members demo what they shipped that week
- *Maturity signal:* Shows who is building new tools (Level 3) vs. using existing ones (Level 2)
- *Audit classification:* Core culture ritual — HIGH encoding risk, never automate
- *Effectiveness:* HIGH. This is Every's primary adoption visibility mechanism. The "be sincere, not serious" ethos makes demos feel like sharing discoveries rather than performing competence.

**2. Published Articles**
- *Function:* Dan and other writers publish practitioner accounts of AI usage
- *Maturity signal:* External accountability — "builder credibility" means you can't write about AI without using it
- *Effectiveness:* HIGH for writers, MEDIUM for non-writing roles. Creates strong incentive for Level 3 behaviors (you need something novel to write about).

**3. Named Personal Agents**
- *Function:* Playful naming convention (R2-C2, Iris, Montaigne, Alfredo, Milo, Claudie, Margot, Droid)
- *Maturity signal:* Having a named agent signals at minimum Level 2 (reusable workflow). The name creates social visibility — "ask Natalia about Claudie" becomes organic knowledge transfer.
- *Effectiveness:* MEDIUM-HIGH. The playful naming aligns with "play as strategy" value and makes AI adoption conversational rather than managerial.

**4. Open-Source Compound Engineering Plugin**
- *Function:* 12K+ GitHub stars, public methodology
- *Maturity signal:* External validation of internal practices
- *Effectiveness:* HIGH for engineering roles, LOW for non-engineering roles.

**5. Consulting Practice as Mirror**
- *Function:* "We practice what we preach" — consulting clients see Every's internal AI practices
- *Maturity signal:* Builder credibility forces real adoption (can't fake it for clients)
- *Effectiveness:* HIGH for consulting-adjacent roles (Natalia, Brooker, Dan), MEDIUM for others.

### Recommended Visibility Additions

**6. Monthly Workflow Show-and-Tell (NEW)**
- *Purpose:* Dedicated session (distinct from demo day) where team members demo *how they work*, not *what they shipped*
- *Format:* 2-3 people, 10 minutes each, show the actual AI workflow — the prompts, the tool chain, the failures, the iteration
- *Maturity signal:* Directly surfaces Level 2 (reusable workflows) and Level 3 (tools others adopt) behaviors
- *Addresses:* Cross-GM knowledge transfer gap (audit: 20 hrs/month lost to reinvention)
- *Cultural fit:* Aligns with "play as strategy" — exploring how you work is inherently playful

**7. Learnings Feed (NEW — Audit Quick Win #3)**
- *Purpose:* Auto-publish new docs/solutions entries from compound engineering's compounding step to a shared #engineering-learnings Slack channel
- *Format:* Automated posts when any GM's compound engineering loop produces new documentation
- *Maturity signal:* Makes compounding behavior (Level 2-3) visible without requiring extra effort
- *Cultural fit:* Passive, async, non-performative — fits Every's low-ceremony culture

**8. Maturity Self-Assessment (NEW)**
- *Purpose:* Quarterly self-assessment using this ladder, shared transparently
- *Format:* Each person self-rates, provides evidence, identifies their own next step
- *Maturity signal:* Self-awareness about adoption level, creates peer accountability
- *Cultural fit:* Must be framed as *curiosity* not *surveillance*. "Where am I?" not "Where should you be?" Aligns with "play as strategy" — self-assessment as discovery. Must explicitly NOT be tied to performance reviews or compensation.

**9. Buddy Pairings for Level Transitions (NEW)**
- *Purpose:* Pair Level 1-2 individuals with Level 3 individuals for specific workflow-building projects
- *Recommended pairings:*
  - Eleanor Warnock + Katie Parrott (editorial AI workflow development)
  - Jack Cheng + Katie Parrott (AI-native writing workflow)
  - Andrey Galko + Kieran Klaassen (shared engineering tool building)
  - Lucas Crespo + Danny Aziz (tool-building mentorship from a fellow builder)
- *Cultural fit:* Aligns with "generalist advantage" — cross-pollination over siloed expertise

---

## Structural Observations

### Why Every's Maturity Is Unusually High

1. **Builder credibility as value:** The top organizational value is "never recommend what you haven't built." This creates existential pressure toward Level 3 — if you write about AI, consult on AI, and sell AI products, you must be a transformative AI user yourself.

2. **GM autonomy model:** Solo GMs running entire products cannot succeed without Level 2+ AI adoption. The structure *requires* AI delegation — a GM managing strategy, engineering, design, metrics, support, and marketing alone simply cannot do it manually.

3. **Small team, high output:** ~20 people producing 272 articles/year, 4 software products, 41 podcast episodes, and $2-3M revenue. The output-to-headcount ratio forces AI amplification at every level.

4. **Founder as practitioner:** Dan Shipper is a Level 3 builder who writes publicly about his AI practice. CEO modeling is the single strongest predictor of organizational AI maturity.

5. **Play as strategy:** Named agents, experimental culture, "be sincere not serious" — AI adoption is framed as fun exploration, not compliance obligation. This eliminates the most common adoption killer: "AI is just another tool management is forcing on us."

### Key Risk: The Level 2 Plateau

Seven team members are at Level 2. The risk is that Level 2 feels "good enough" — personal agents work, AI delegation is habitual, productivity is high. The jump to Level 3 requires building something *others use*, which demands different skills (tool design, documentation, evangelism) than personal workflow optimization. Every should watch for Level 2 plateau signals:
- "My workflow works great for me" without sharing it
- Using AI tools without modifying or extending them
- Declining to demo at show-and-tell because "I didn't build anything new"

The recommended visibility mechanisms (show-and-tell, learnings feed, buddy pairings) are specifically designed to create gentle upward pressure from Level 2 to Level 3.

---

## Appendix: Assessment Confidence

| Person | Confidence | Notes |
|--------|-----------|-------|
| Dan Shipper | HIGH | Extensive public evidence (articles, products, agents) |
| Brandon Gell | MEDIUM | Evidence from audit + values doc, limited public behavioral data |
| Kate Lee | MEDIUM-HIGH | Audit bottleneck data + AI tells evidence |
| Eleanor Warnock | MEDIUM | Audit bottleneck data, limited tool-building evidence |
| Katie Parrott | HIGH | Clear Level 3 artifacts (detection skills, "sculpture" framework) |
| Kieran Klaassen | HIGH | Compound engineering methodology is definitive Level 3 |
| Naveen Naidu | HIGH | 143K-line solo codebase is definitive evidence |
| Yash Poojary | HIGH | AgentWatch + parallel sessions + learnings docs |
| Danny Aziz | HIGH | Droid CLI + Spiral v3 solo + Cursor abandonment |
| Andrey Galko | MEDIUM | Tool switch evidence, limited workflow artifact evidence |
| Nityesh Agarwal | MEDIUM | Pre-research discipline clear, tool-building evidence limited |
| Natalia Quintero | HIGH | Claudie with measurable impact (14 hrs/week) |
| Brooker Belcourt | MEDIUM-LOW | Compound engineering for clients noted, specific artifacts unclear |
| Lucas Crespo | MEDIUM | Alfredo agent + Figma MCP clear, broader tool-building evidence limited |
| Austin Tedesco | MEDIUM | Montaigne agent + Proof usage clear, system-building evidence limited |
| Anukshi Mittal | MEDIUM-LOW | Iris agent noted, specific workflow artifacts unclear |
| Rachel Braun | MEDIUM | Descript + StreamYard usage clear, custom tool-building evidence limited |
| Anthony Scarpulla | HIGH | Custom Claude Code + X API integration is definitive Level 3 |
| Jack Cheng | MEDIUM-LOW | Contributing editor with limited visibility into AI practices |

---

*Generated by maturity-ladder skill, ai-first-org-design-kit.*
*Input data: coordination audit (2026-04-01), VALUES.md, team behavioral evidence.*
*Next recommended skill: adoption-sprint-designer — design a sprint targeting the Level 2 to Level 3 transition for the 7 team members at Level 2.*
