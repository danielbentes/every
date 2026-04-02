---
title: "Your Agents Don't Know Who You Are"
layout: default
nav_order: 2
---

# Your Agents Don't Know Who You Are

Every organization runs on an operating system. Not the kind you install — the kind that lives in the CEO's head. The anthropologist Clifford Geertz called culture "the stories people tell themselves about themselves." Organizations are the same. They run on stories about how we work that have never been written down. The unwritten rules about what "quality" means, who decides what, when to ship and when to hold, what you'd never do regardless of the upside. At most companies, this operating system has never been written down. It doesn't need to be, because it travels through hallway conversations and shared instincts.

That worked fine for 150 years of organizational management. It breaks the moment you deploy an AI agent.

Every has about 20 people. We run four AI software products each managed by a single person, publish a daily newsletter to 100,000+ subscribers, and operate a seven-figure consulting practice. Ninety-nine percent of our code is written by AI agents. Our organizational OS has been running in my head, in **Kate Lee's** editorial instincts (she's our Editor in Chief, formerly publisher of Stripe Press), in **Kieran Klaassen's** compound engineering methodology, in **Natalia Quintero's** consulting client relationships. It works because we're small enough that judgment travels through Slack and demo day.

But our agents can't attend demo day. When R2-C2 (my personal AI agent) drafts a response, it doesn't know that builder credibility is our absolute tiebreaker value. When Claudie (Natalia's AI project manager) generates a client status report, it doesn't inherently understand that consulting data from Client A can never inform work for Client B. When our compound engineering agents auto-fix a bug, they don't know that "code without compound" — shipping a feature without documenting what the system learned — is an anti-pattern we reject on sight.

The hardest part of going AI-first isn't the technology. It's encoding the taste, judgment, and identity that makes your organization *yours* into a format agents can actually use. I ran a 14-skill organizational design toolkit on Every to do exactly that. Here's what it produced, what I learned, and how you can do it for your company.

---

## What We Did: 14 Skills, One Organizational Genome

The [AI-First Org Design Kit](https://github.com/synaptiai/synapti-marketplace/tree/main/plugins/ai-first-org-design-kit) is a structured toolkit with 14 skills that walk you from organizational diagnosis to agent deployment. Each skill asks interview questions designed to force articulation of tacit knowledge, the things everyone "just knows" but no one has written down.

The process follows a deliberate sequence:

1. **Coordination Audit:** Quantify where human time actually goes
2. **Org Genome Builder:** Encode identity as decision rules, voice norms, quality standards
3. **Political Navigator:** Map who holds power and how to reframe the change
4. **Quality Gate Designer:** Convert subjective approvals into criteria-based gates with hidden tests
5. **Specification Writer:** Write workflow specs precise enough for someone with zero context
6. **Role Value Mapper:** Define every role around specification responsibility
7. **Governance Architect:** Build the ecosystem: authority tiers, boundaries, escalation, learning loop
8. **Operationalize:** Distill everything into a 206-line primer any agent can load
9. **Maturity Ladder:** Assess where each person actually is in AI adoption
10. **Adoption Sprint Designer:** Design sprints that convert Level 2 users into Level 3 tool-builders
11. **Usage Policy Writer:** Create a human-facing AI policy with risk reasoning
12. **Agent Builder:** Generate role-specific agent configs with system prompts and self-review
13. **Holdout Evaluator:** Validate agent output against hidden holdout scenarios with LLM-as-judge
14. **Evolution Auditor:** Establish baselines and set up the monthly governance review cycle

Each skill produces structured markdown files. Together they form a complete organizational specification: 52 files totaling nearly 7,000 lines of operating instructions, quality standards, governance rules, and agent configurations. All discoverable by downstream skills, all cross-referenced, all grounded in Every's actual practices.

The interview questions are where the real work happens. "Name 3-5 things your organization genuinely values. Not wall-poster values, things that actually drive decisions when things get hard." "When two of your values conflict, which one wins? Walk me through a real example." "What should an agent NEVER decide on its own?" These are questions most CEOs have never been asked. Answering them well is the difference between a genome agents can operate from and a document that sounds nice but tells an agent nothing useful.

---

## The Genome: Values as Operating Instructions

The organizational genome is seven files that encode who Every is. Not the marketing version — the operational version. The process of building it felt like a therapy session crossed with a systems architecture review.

The most important file is `VALUES.md`. Most companies list values like "integrity" and "innovation." The genome builder doesn't let you get away with that. For each value, it demands: a decision rule, a real example where the value determined a decision, what you sacrificed by choosing it, and what happens when it conflicts with another value. Here are ours:

**1. Taste Over Process.** Trust demonstrated judgment over checklists. If output feels "technically correct but not right," flag it — that gap is where taste lives. Customer-facing output: taste wins. Internal artifacts: speed wins.

**2. Ship and Iterate.** Default to shipping. If the core flow works, ship v1 with known rough edges. Spiral's first version was built in two days. **Danny Aziz** shipped Spiral v3 as a single engineer with Claude Code support. We sacrifice polish for learning velocity. (Investors sometimes find this alarming. We find it clarifying.)

**3. Builder Credibility.** Never recommend tools we haven't used ourselves. Never assert "AI can do X" without referencing how Every has actually done X. This is the absolute tiebreaker — it beats every other value when they conflict. We've turned down lucrative consulting deals because the engagement would have required recommending tools we don't use internally.

**4. Generalist Advantage.** Writers build software, engineers write articles. Every GM runs their entire product solo. We sacrifice specialist depth for the breadth that lets each person see connections specialists miss.

**5. Play as Strategy.** "Be sincere, not serious." We named our AI agents R2-C2, Iris, Montaigne, Margot, Alfredo, and Milo. Our funding round was "large enough that our investors will answer the phone, and small enough that we can keep being weird."

The priority ordering matters more than the individual values: builder credibility beats taste, taste beats speed, speed beats generalist breadth, breadth beats play. This means we'd delay a ship to protect taste, and we'd sacrifice taste on internal tools to ship faster, but we'd never ship anything — fast or polished — that undermines our builder credibility.

The genome also includes `VOICE.md`, which encodes how Every communicates. Words we use: "allocation economy," "compound engineering," "taste," "ship," "builder." Words we never use: "leverage," "synergy," "cutting-edge," "we're excited to announce." AI tells to reject: "Moreover," "Furthermore," "It's worth noting," vague pronouns, unsourced claims. The three rigor tests every article must pass: articulates something true, offers learnable value, sounds authentically like the writer.

And `BY-OUTPUT-TYPE.md`, which defines quality per output type. Articles need a specific thesis in the first three paragraphs. Code needs a compound artifact, because the system must learn from every PR. Consulting deliverables need hands-on building, not slides. Social posts must capture the article's actual argument, not just tease it.

None of this is aspirational. Every standard comes from a real decision we made, a real thing we shipped, a real deal we turned down. The genome template forces concrete examples for every value. If you can't give one, the value is aspirational, not operational. And it gets marked as such.

---

## Nine Boundaries an Agent Can't Cross

The genome tells agents who we are. Governance tells them where the walls are. I expected governance to be the bureaucratic part, the compliance exercise you endure before getting to the interesting work. I was wrong. Defining boundaries turned out to be clarifying in a way I didn't anticipate. When you write down what an agent must never do, you discover what you actually care about protecting.

Governance at Every is six interconnected documents. The most critical is `HARD-BOUNDARIES.md`, nine lines agents can never cross regardless of context, urgency, or perceived benefit:

1. Never publish without human editorial review
2. Never send external communications to clients or partners
3. Never make financial commitments
4. Never access or share client data across engagements
5. Never merge to production without the review gate passing
6. Never change another GM's configuration
7. Never exceed the product's defined PII scope
8. Never make claims not backed by Every's actual experience
9. Never bypass quality gates, even under time pressure

Each boundary has a violation protocol: halt immediately, log to the decision ledger, escalate to the appropriate human, do not retry until the human reviews. Boundaries can only be modified through the governance learning loop: three or more logged friction instances, a proposal, monthly review by Dan and Brandon, unanimous stakeholder approval. No individual can override a boundary in the moment.

The authority matrix defines four tiers. Tier 1 (Autonomous): bug triage, code generation within an approved plan, research, internal drafts. Tier 2 (Autonomous + Notify): bug auto-fixes before the GM reviews, pipeline nudges to writers, client status reports. Tier 3 (Human-in-Loop): article publication (Kate Lee approves, 48-hour hold, never auto-publishes), code merge (GM approves, 24-hour hold), consulting deliverables (Natalia approves). Tier 4 (Human-Only): hiring, strategy, finances, client confidential matters, editorial direction.

The rule that ties it together: no Tier 3 action ever auto-executes. Hold means hold. If the human doesn't respond, the action waits. This feels conservative. It is. Missing a deadline is always preferable to an agent making a decision it shouldn't. (We can loosen later with evidence. We can't un-send a bad email to a hedge fund CIO.)

The other four governance documents complete the ecosystem. Escalation protocols define when and how agents surface decisions to humans, with a structured format designed for two-minute decisions. The policy generation loop defines how governance grows when agents encounter novel situations. The decision ledger records every Tier 2+ decision in an append-only log. And the learning loop defines the monthly governance review cycle that evolves all of this from operational evidence.

---

## Quality Gates with Hidden Tests

We designed four quality gates, each with hidden holdout scenarios the executing agents never see.

The **article publication gate** encodes Kate Lee's editorial judgment into pass/fail criteria. This is the gate I'm most nervous about, because it attempts to operationalize taste, which is the thing I've always said can't be operationalized. Tier 1 (blocking): thesis in the first three paragraphs, no AI tells, grounded in first-hand experience, authentic author voice, sufficient depth. Tier 2 (advisory, flagged for Kate): learnable value, originality, builder credibility. The gate doesn't replace Kate. It expands her bandwidth. The estimated 70% of articles that clearly pass or clearly fail don't need her time. She focuses on the borderline cases where irreducible taste judgment matters.

The **code merge gate** formalizes our compound engineering review. All tests must pass, all Priority 1 findings from the 14 review agents must be resolved, the implementation must follow the approved plan (or deviations must be documented), and at least one compound artifact must be produced. That last criterion is the one that matters most: the system must learn from every PR. A feature that ships without documentation isn't done.

Each gate has holdout scenarios stored in a separate hidden directory. Test cases the executing agent never sees. The article gate has seven. One is AI slop that sounds sophisticated. One is great writing with no thesis. One is legitimately excellent (to test that the gate doesn't over-filter, because a gate that rejects good work is worse than no gate at all). Agents running the gate never read these scenarios. They exist to test whether the gate criteria actually catch what they're supposed to catch. Think of them like a teacher's answer key that the student never sees.

---

## Where Every Team Actually Is

The maturity ladder assessed 19 people across four levels. Level 0: not engaged (no one at Every). Level 1: capable, uses AI for multiple tasks weekly. Level 2: adoptive, has designed at least one reusable AI workflow and delegates execution to AI by default. Level 3: transformative, has built or extended an AI tool that others now use.

Every's distribution: nine people at Level 3 (47%), seven at Level 2 (37%), two transitioning between Level 1 and 2, and one at Level 1. Organizational mean: 2.4 out of 3. No one at Level 0.

The interesting finding is the Level 2 plateau. Seven people whose personal AI workflows work brilliantly but who haven't crossed into building tools others use. The jump from "AI makes me faster" to "I create capabilities for the team" requires different skills: tool design, documentation, evangelism. The adoption sprint we designed targets exactly this: a three-day internal hackathon where each Level 2 participant is paired with a Level 3 buddy, builds one reusable artifact, and demos it on the final day. The forcing function is the demo — you can't present what you didn't build.

We also designed a consulting client template based on the internal sprint. Every's consulting practice has run eight camps with 5,395 participants. The sprint template standardizes that into a structured two-day format with buddy pairing, hands-on building (never slides), and a mandatory demo where every participant presents.

---

## What This Actually Produces

The capstone is operationalization: distilling everything into formats agents and humans can use daily.

The **AGENT-PRIMER.md** is 206 lines that compress nearly 7,000 lines of organizational specification into actionable operating rules. Every line answers "what should I do?" or "what should I never do?", not "why was this designed this way?" An agent loading the primer at session start knows Every's mission, values with priority ordering, voice norms, quality standards per output type, all nine hard boundaries, the four-tier authority model, escalation routing, quality gate criteria, and governance operations (how to handle novel situations, record decisions, and classify failures).

The **CLAUDE.md** with @imports auto-loads mission, values, and hard boundaries at every Claude Code session start. This means every agent working in Every's codebase has the organizational foundation in context without anyone having to remember to paste it.

Five **governance skills** are invokable as `/org-voice-check` (review output against voice norms), `/org-gate-review` (self-review against a quality gate), `/org-record-decision` (append to the decision ledger), `/org-values-check` (evaluate a decision against the value hierarchy), and `/org-novel-situation` (draft a candidate policy for situations governance doesn't cover yet).

Five **agent configurations** (editorial quality, compound engineering, consulting PM, content distribution, and product GM), each with a system prompt, tool permissions, and self-review checklist mapped to their applicable quality gate.

And a **living evolution loop**: monthly governance review, decision ledger tracking every consequential agent decision, and a learning loop that evolves governance from operational evidence rather than committee meetings.

---

## What I Learned

The hardest question in the entire process was this: "What does 'taste' actually mean when an agent has to apply it?"

I've been using the word "taste" to describe what makes Every's output good for years. Kate Lee has taste. Kieran's compound engineering has taste. Our articles have a taste that readers recognize. But when the genome builder asked me to encode taste as a decision rule an agent could follow, I had to sit with how little I'd actually articulated. I wrote "The Allocation Economy" arguing that AI shifts value toward vision, taste, and evaluation ability. Running the genome builder is that argument applied to yourself. The excavation — pulling implicit knowledge out of your own head and making it operational — is harder than any technology decision I've made at Every.

Here's what surprised me once I got through it.

Values are useless until they conflict. "We value quality" tells an agent nothing. But "when quality conflicts with speed, quality wins for customer-facing output and speed wins for internal artifacts — and builder credibility beats both regardless" is an operating instruction an agent can follow. I spent more time on the conflict resolution rules than on the values themselves, and the conflict rules turned out to be more valuable. An agent that knows the priority ordering — builder credibility, then taste, then speed, it can resolve most judgment calls without escalating.

The nine hard boundaries were faster to define than the values but have more operational impact. What should agents never do? Never publish without human review. Never share client data across engagements. Never bypass quality gates even under time pressure. An agent loaded with just those nine lines has a safety floor that prevents catastrophic failures. Everything else is optimization on top of that floor.

I assumed governance was a one-time exercise. Write the rules, ship them, move on. Wrong. Static rules fossilize. The part of the governance ecosystem that matters most isn't the hard boundaries. It's the learning loop. Agents encounter novel situations, draft candidate policies, and log them. The decision ledger tracks what actually happened. Brandon and I review the ledger the first Monday of each month. Governance that doesn't evolve becomes either obsolete (agents work around it) or oppressive (it blocks legitimate work).

And then the maturity ladder showed me something I genuinely didn't expect. I knew our team was AI-native. What I didn't know was where the specific frontier was. Seven of our twenty people sit at Level 2 — they use AI brilliantly for their own work but haven't crossed into building tools others use. The jump from "AI makes me faster" to "I create capabilities for the team" is the adoption gap that matters most right now. Training doesn't bridge it. Sprints do. Three days, buddy pairing with someone who's already crossed, build one real thing, demo it on day three.

---

## How to Do This for Your Organization

You don't need fourteen skills in one session. Start with two:

**First, build your genome.** Run the org genome builder. Answer the eleven questions honestly. Not the marketing version. The operational version. Encode your values as decision rules with conflict resolution. Define your voice. Set quality standards per output type. Apply the Stranger Test: could someone with zero context about your organization read this genome and produce output you'd accept?

**Second, define your hard boundaries.** Run the governance architect. Paint the nightmare scenario: the worst thing an agent could do in your organization. Work backward from there to define the lines that can't be crossed. Design the four-tier authority model. Build the escalation protocols.

Those two skills produce the minimum viable organizational specification. An agent loading your genome and hard boundaries has a values foundation and a safety floor. Everything else (quality gates, workflow specs, role definitions, maturity assessment, adoption sprints, agent configurations, evolution audits) enriches that foundation as you grow.

The Stranger Test is the quality bar throughout: could a hyper-competent new hire, or a new agent, operate with your judgment from day one? If not, the specification isn't done. Keep articulating until it is.

The exercise took one session and produced 52 files. The files are useful. But the most valuable output wasn't the files. It was the forced articulation of things I'd been deciding on instinct for six years. The next twenty people we hire can read this instead of spending six months absorbing it through osmosis. Consulting clients can see how we actually operate instead of guessing. And I finally had to confront what I actually believe about how this company should work — which turned out to be slightly different from what I thought I believed.

Your organization already has an operating system. It's just running in your head. The question is whether you're going to encode it before or after your agents start making decisions without it.