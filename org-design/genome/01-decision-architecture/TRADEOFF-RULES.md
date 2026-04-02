---
title: Tradeoff Rules
layout: default
parent: Genome
nav_order: 5
---

# Value Conflict Resolution Rules

When organizational values conflict, use these rules to decide.

## Rule: Taste vs. Speed

**When they conflict:** A piece of content, product feature, or deliverable is "good enough" to ship but doesn't meet the quality bar that represents Every's best.

**Default winner:** Depends on audience.

**Resolution:**
- **Customer-facing content (articles, social, podcast)** → Taste wins. Delay publication rather than ship something that doesn't pass the three rigor tests or sounds like AI slop.
- **Software products (features, bug fixes)** → Speed wins if core flow works. Ship v1, iterate. Known rough edges are acceptable; broken core flows are not.
- **Consulting deliverables** → Taste wins. Client trust is at stake. Never deliver something that undermines our builder credibility.
- **Internal artifacts (CLAUDE.md, docs, Slack)** → Speed wins completely. No taste gate on internal communication.

**Example:**
> Katie Parrott's AI tells detection flags an article as having formulaic transitions and hedging language. Publication deadline is today.
> Decision: We delay. The article goes through another revision cycle. Our readers trust us because we don't sound like AI wrote our content about AI.

---

## Rule: Builder Credibility vs. Revenue

**When they conflict:** A lucrative opportunity (consulting deal, sponsorship, content partnership) would require us to recommend, promote, or appear to endorse something we don't genuinely use or believe in.

**Default winner:** Builder credibility. Always.

**Resolution:**
- **Builder credibility always wins.** No revenue justifies undermining the trust that makes all future revenue possible.
- **No exceptions.** We've turned down consulting deals that would have required recommending tools we don't use. We'll do it again.

**Example:**
> A large enterprise wants us to consult on adopting a specific AI tool we don't use internally and don't believe is best-in-class.
> Decision: We decline the engagement. We suggest they find a consultant who actually uses that tool. We might recommend alternatives from our own stack.

---

## Rule: Generalist Breadth vs. Specialist Depth

**When they conflict:** A task requires deep specialist knowledge that no one on the team currently has, and hiring a generalist won't solve it fast enough.

**Default winner:** Generalist for permanent roles, specialist for targeted needs.

**Resolution:**
- **Hiring permanent team members** → Generalist wins. We'd rather teach someone a specific skill than teach someone to think broadly.
- **Solving specific technical challenges** → Specialist knowledge wins. Bring in external freelancers (e.g., Cora's external senior full-stack engineer for complex infrastructure).
- **AI agents** → Specialist by design. Agents can go deep in narrow domains; humans should stay broad.

**Example:**
> Cora needs complex infrastructure work beyond what GM Kieran can handle with AI assistance alone.
> Decision: Bring in an external senior engineer (part-time, specialized) rather than hiring a full-time backend specialist. Kieran stays as generalist GM.

---

## Rule: Play vs. Professionalism

**When they conflict:** A playful, personality-rich approach risks being perceived as unserious by an important external audience.

**Default winner:** Play, with audience awareness.

**Resolution:**
- **Articles and content** → Play wins. Personality IS our brand. "Be sincere, not serious."
- **Internal communication** → Play wins always. Name your agents fun things. Use emojis. Have fun.
- **Consulting client interactions** → Adjust to client culture. A hedge fund CIO expects different energy than a startup CTO. But never lose authenticity — even in conservative contexts, our warmth and directness should come through.
- **Legal/financial/contractual** → Professionalism wins. Don't be cute with contracts.

**Example:**
> We're presenting to a conservative financial services firm. Brandon wants to lead with our usual casual, playful style.
> Decision: We tone down the casual elements but keep the directness and builder credibility front and center. We don't pretend to be a Big Four firm, but we don't show up in hoodies either. The substance is unchanged; the packaging adapts.

---

## Rule: GM Autonomy vs. Company Consistency

**When they conflict:** A product GM wants to make a decision that's right for their product but inconsistent with how other products or the broader company operates.

**Default winner:** GM autonomy, unless it affects shared resources or brand.

**Resolution:**
- **Product decisions (features, roadmap, technical stack)** → GM autonomy wins. Each GM owns their product entirely. Yash uses Codex+Claude in parallel; Danny uses Droid CLI; Naveen lives in Linear. That diversity is a feature, not a bug.
- **Brand and voice** → Company consistency wins. All products are Every products and should feel like it.
- **Shared resources (design team time, infrastructure)** → Company coordination wins. The design team rotation model exists because resources are shared.
- **Customer data and privacy** → Company policy wins. Individual GMs cannot make exceptions to data handling policies.

**Example:**
> Danny (Spiral GM) wants to implement a completely different onboarding flow that doesn't match the pattern used by Cora and Sparkle.
> Decision: Danny has full autonomy on Spiral's onboarding. Products don't need to look the same. But if it touches shared subscription/billing infrastructure, coordinate with the platform team.

---

## Priority Ordering (Ultimate Tiebreaker)

When multiple values apply simultaneously:
1. **Builder credibility** — absolute priority. Never compromised under any circumstances.
2. **Taste over process** — for customer-facing output. Our reputation depends on this.
3. **Ship and iterate** — for everything that isn't customer-facing. Speed is our competitive advantage.
4. **Generalist advantage** — in hiring and role design. Shapes who we are long-term.
5. **Play as strategy** — in culture and communication. Makes work enjoyable and attracts talent.

## Agent Instructions for Conflict Resolution

When facing a value conflict:
1. Identify which values are in tension
2. Check this document for a specific rule covering the scenario
3. If a specific rule exists → follow it
4. If no rule exists → escalate to the relevant human (GM for product decisions, Kate for editorial, Natalia for consulting, Dan for company-wide)
5. Present both options clearly: "Value A suggests X. Value B suggests Y. Here's my assessment of the tradeoff."
6. Log the conflict and resolution for future rule creation (append to decision ledger)
