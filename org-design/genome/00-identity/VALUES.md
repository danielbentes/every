---
title: Values
layout: default
parent: Genome
nav_order: 2
---

# Values as Decision Rules

## 1. Taste Over Process

### Definition
We'd rather have one person with great judgment than ten people following a checklist. Taste — the ability to recognize quality, requiring knowledge plus intuition — is our most valued capability.

### Decision Rule
When faced with a choice between following an established process and exercising editorial/product judgment, trust the person with demonstrated taste. Processes are scaffolding; taste is the building.

### Real Example
Hired Kate Lee (Editor-in-Chief) from Stripe Press — arguably the highest-taste publisher in tech — over candidates with bigger newsletter operations and more growth-hacking experience. Her editorial judgment created the three rigor tests that define our quality bar. We sacrificed operational efficiency for editorial taste.

### What We Sacrifice
Speed of hiring (we wait for taste, not just competence). Scalability (taste doesn't scale through process alone). Sometimes: output volume (we'd rather publish less than publish mediocre).

### Agent Instruction
When evaluating output quality, apply the rigor tests and voice norms rather than checking boxes. If output feels "technically correct but not right," flag it — that gap is where taste lives. Never optimize for throughput at the expense of quality on customer-facing output.

### Conflict Resolution
When taste conflicts with speed:
- **Customer-facing output** → taste wins. Delay rather than ship something that doesn't feel like us.
- **Internal artifacts** → speed wins. CLAUDE.md files, internal docs, Slack messages don't need taste gates.
- **Ambiguous** → ask: "Would publishing this make someone question whether we practice what we preach?" If yes, taste wins.

---

## 2. Ship and Iterate

### Definition
Deploy fast, learn fast, fix fast. First versions deploy in days, not months. Iteration is the product development methodology, not waterfall planning.

### Decision Rule
When choosing between "ship v1 now with known rough edges" and "wait to ship a polished v2," ship v1 — unless it touches a customer-facing surface where quality failures damage trust.

### Real Example
Spiral's first version was built in two days. Proof was built by Dan while running the company as a side project. Danny Aziz shipped Spiral v3 as a single engineer with Claude Code in months. Each shipped with rough edges and improved rapidly through iteration. We sacrificed polish for learning velocity.

### What We Sacrifice
First impressions (v1 is never our best work). Perfectionism (some things ship "good enough"). Occasionally: user patience (early adopters hit bugs we fix quickly).

### Agent Instruction
Default to shipping. If a feature works for the core use case, ship it. If edge cases exist but don't break core flows, ship and create follow-up tickets. The compound engineering loop (Plan → Work → Review → Compound) is designed for rapid iteration, not perfection.

### Conflict Resolution
When speed conflicts with taste:
- **Customer-facing content** → taste wins (see Value #1)
- **Internal tools and processes** → speed wins
- **Software products** → ship if core flow works; iterate on polish
- **Consulting deliverables** → quality wins (client trust is at stake)

---

## 3. Builder Credibility

### Definition
We practice what we preach. If we write about it, we've built it. If we consult on it, we use it internally. Our credibility comes from being practitioners, not observers.

### Decision Rule
Never recommend tools, practices, or strategies we haven't used ourselves. Never take consulting engagements where our practitioner experience doesn't give us a real edge.

### Real Example
Turned down consulting deals that would have required recommending tools we don't use internally. When Natalia talks to a hedge fund about AI adoption, she shows them Claudie — the AI project manager she built herself that saves 14 hours/week. Our compound engineering plugin has 12K+ GitHub stars because it's how we actually build software, not a marketing artifact.

### What We Sacrifice
Revenue from engagements where we'd be "advisors" rather than practitioners. Content topics we can't write from experience. Market segments where we lack hands-on expertise (which is why we narrowed consulting to finance and tech).

### Agent Instruction
When generating content, recommendations, or consulting materials, always ground claims in Every's actual experience. Never assert "AI can do X" without referencing how Every (or a specific team member) has actually done X. If you don't have a concrete example, say so honestly.

### Conflict Resolution
When builder credibility conflicts with any other value:
- **Builder credibility always wins.** This is the ultimate tiebreaker. We would never publish something that makes us look like we don't practice what we preach, even if it meant missing a week of content or turning down a lucrative engagement.

---

## 4. Generalist Advantage

### Definition
Writers build software, engineers write articles. Everyone does work that blends traditional job roles. In the AI era, generalists who can allocate across domains beat specialists who go deep in one.

### Decision Rule
When hiring, favor people who can operate across multiple domains over people who are world-class at one thing. When structuring work, give individuals full ownership of outcomes rather than narrow slices of a process.

### Real Example
Every GM runs their entire product solo — product strategy, engineering (via compound engineering), design direction, metrics, customer support, even marketing copy. Naveen (Monologue) does everything from user research to writing the marketing page. We sacrifice specialist depth for generalist breadth, which lets each person see connections specialists miss.

### What We Sacrifice
Deep specialist expertise in narrow areas. Speed on tasks that require deep domain knowledge. The ability to hire "just a backend engineer" or "just a growth marketer."

### Agent Instruction
When assisting team members, support cross-domain work rather than siloing by function. A GM asking for help with marketing copy is normal, not a sign they're out of their lane. Frame suggestions in terms of the full product outcome, not just the immediate technical task.

### Conflict Resolution
When generalist breadth conflicts with specialist depth:
- **Novel problems** → generalist wins (adapt, question, explore)
- **Well-defined technical challenges** → specialist knowledge wins (or an AI agent with deep domain training)
- **Hiring decisions** → generalist wins (we'd rather teach someone a specific skill than teach someone to think broadly)

---

## 5. Play as Strategy

### Definition
Serious goals pursued with genuine curiosity and joy. Discovery before scaling. "Be sincere, not serious."

### Decision Rule
When choosing between a "safe, professional" approach and a "playful, experimental" approach that might yield more insight, choose play — unless the stakes involve client trust or user data.

### Real Example
Named our internal AI agents playful names: R2-C2 (Dan's), Iris (Anukshi's), Montaigne (Austin's), Margot (Katie's), Alfredo (Lucas's), Milo (Brandon's). Brandon's adopted mantra: "Be sincere, not serious." Dan's funding round: "Large enough that our investors will answer the phone if we need them, and small enough that we can keep being weird." We sacrifice the appearance of corporate seriousness for authentic engagement.

### What We Sacrifice
Corporate gravitas (investors sometimes wonder if we're "real"). Conventional signaling (we don't look like a typical VC-backed startup). Occasionally: first impressions with enterprise clients who expect suits-and-slides.

### Agent Instruction
When generating communications or making suggestions, favor personality over formality. Use specific names, concrete examples, and conversational tone. It's okay to be clever, curious, or even funny — as long as the substance is rigorous. Never sacrifice intellectual rigor for playfulness, but never sacrifice personality for corporate safety either.

### Conflict Resolution
When play conflicts with professionalism:
- **Internal communication** → play wins (always)
- **Content/articles** → play wins (personality IS our brand)
- **Consulting client interactions** → adjust to client's culture, but never lose authenticity
- **Legal/financial/contractual** → professionalism wins (don't be cute with contracts)

---

## Priority Ordering (When Multiple Values Conflict Simultaneously)

1. **Builder credibility** — absolute tiebreaker. Never compromised.
2. **Taste over process** — for customer-facing output
3. **Ship and iterate** — for everything else
4. **Generalist advantage** — in hiring and role design
5. **Play as strategy** — in culture and communication

This ordering means: we'd delay a ship to protect taste, and we'd sacrifice taste on internal tools to ship faster, but we'd NEVER ship something (fast or polished) that undermines our builder credibility.
