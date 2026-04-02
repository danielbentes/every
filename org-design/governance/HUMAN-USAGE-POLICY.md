---
title: Human Usage Policy
layout: default
parent: Governance
nav_order: 7
---

# AI Usage Policy — Every Inc

*For Humans -- v1.0 -- 2026-04-01*
*Review cadence: Quarterly (next: 2026-07-01)*

## Purpose
This policy defines what AI tools are approved, what data can go into them, and the reasoning behind each rule. It applies to everyone at Every — writers, editors, engineers, consultants, marketing, design.

For agent-specific operating rules, see: `governance/HARD-BOUNDARIES.md`
For the full organizational primer, see: `AGENT-PRIMER.md`

## Executive Summary
Use approved tools freely with public and internal data. Confidential data (client, financial) requires explicit authorization from Natalia or Dan. Client data never crosses engagements. When in doubt, ask — it's always the right call.

---

This policy is for you, the person reading it. Not an agent, not a bot, not a CLAUDE.md file. You.

Every is an AI company. We use AI constantly, proudly, and seriously. That means we need shared rules about how we use it -- not because we're afraid of AI, but because we're practitioners. We know what can go wrong, and we know that sloppy AI use from an AI company is the fastest way to lose credibility.

Read this once. Refer back when you're unsure. Ask questions in #engineering-learnings or ping the relevant person directly.

---

## What We Use and What It's For

These are Every's approved AI tools. If you want to use something not on this list, see the exception process below.

### Models and Assistants

| Tool | What We Use It For |
|------|-------------------|
| **Claude** (Claude Code, API) | Primary AI model. Engineering, editorial assistance, consulting prep, internal automation. Our default. |
| **ChatGPT / GPT models** | Writing assistance, research, brainstorming, second opinions. |
| **Codex** (OpenAI) | Engineering work, brainstorming approaches, draft PRs. |
| **Droid CLI** (Factory.ai) | Engineering -- Danny's primary tool for Spiral development. |

### Every's Own Products

| Tool | What It Does |
|------|-------------|
| **Spiral** | AI writing partner. Use it for drafts, rewrites, ideation. |
| **Cora** | Email management. Handles inbox triage and responses. |
| **Monologue** | Voice dictation. Turns spoken words into structured text. |
| **Sparkle** | File organization. Keeps your digital workspace clean. |
| **Proof** | Document editing with provenance tracking. Green highlights = human, purple = AI. |

### Agents and Integrations

| Tool | What It Does |
|------|-------------|
| **Plus One / OpenClaw** | Personal AI agents in Slack. Help with tasks, answer questions, automate workflows. |
| **Descript** | Podcast and audio editing for AI & I and other audio work. |
| **Figma MCP** | Design integration for compound engineering workflows. |
| **Sentry MCP** | Error monitoring integration. |
| **Linear MCP** | Project management integration -- connects agents to our source of truth for product work. |

---

## Data Classification: What Goes Where

This is the part that matters most. Read it carefully.

### Public Data -- Any Approved Tool

Articles, published essays, marketing copy, open-source code, anything already visible to the world. Paste it into any approved tool without hesitation.

### Internal Data -- Approved Tools with Enterprise Agreements Only

Product source code, internal Slack conversations, internal docs, draft articles, compound engineering configs, CLAUDE.md files, meeting notes.

These can go into approved tools listed above -- they all have appropriate data handling agreements. But do not paste internal data into random AI tools you found on Product Hunt. If it's not on the approved list, it's not approved.

### Confidential Data -- NEVER Without Explicit Authorization

This includes:

- **Client engagement data** (consulting deliverables, client workflows, client-specific analysis)
- **Financial data** (revenue numbers, runway, investor communications, compensation)
- **User PII** (subscriber emails, payment information, usage analytics tied to individuals)

**The rule is simple:** Do not enter confidential data into any AI tool without explicit authorization from:
- **Natalia** -- for anything related to consulting clients
- **Dan** -- for anything financial

Not "I think it would be fine." Not "It's just one data point." Ask first.

### Restricted Data -- NEVER Share Cross-Engagement

Client-specific data from consulting engagements is siloed. What we learn working with Client A never goes into a prompt, a document, or a conversation about Client B. Not even within Every. Not even anonymized without Natalia's review.

This is the hardest rule to follow because it's the most tempting to bend. "But the pattern is so relevant..." Doesn't matter. Client trust is sacred. One breach and we lose not just that client but the entire consulting practice.

---

## Why These Rules Exist (Risk Model)

We don't do policy for policy's sake. Here's the actual reasoning behind each rule category:

### Rule: Approved Tools Only

| Dimension | Assessment |
|-----------|-----------|
| **Why** | Unapproved tools may not have enterprise data agreements, could expose internal code/data to unknown third parties |
| **Risk** | Internal data exposed to tools without proper data handling agreements |
| **Likelihood** | Medium — new AI tools launch weekly and are tempting to try |
| **Impact** | Medium — data exposure risk, but internal data is less sensitive than client data |
| **Decision** | Use approved tools only. Request exceptions through the exception process for new tools. |
| **When this applies** | Any time you're about to use an AI tool not on the approved list above |

### Rule: Confidential Data Requires Authorization

| Dimension | Assessment |
|-----------|-----------|
| **Why** | Client data, financial data, and user PII are trust-critical. A single exposure damages relationships that took years to build |
| **Risk** | Client or financial data entered into an AI tool leaks or is used for model training |
| **Likelihood** | Low — if the rule is followed. High — if people start making individual judgment calls about "this one is probably fine" |
| **Impact** | Critical — one consulting client data breach could end our entire consulting practice ($1-2M revenue) |
| **Decision** | Explicit authorization from Natalia (client data) or Dan (financial data) before any confidential data enters any AI tool |
| **When this applies** | Any time you're about to input data related to a client engagement, company finances, or identifiable user information |

### Rule: Client Data Never Crosses Engagements

| Dimension | Assessment |
|-----------|-----------|
| **Why** | Consulting clients trust us with sensitive operational data. Cross-contamination — even anonymized — erodes that trust |
| **Risk** | Patterns, insights, or specific data from Client A influence work for Client B |
| **Likelihood** | Medium — the temptation is high because "the pattern is so relevant" |
| **Impact** | Critical — if discovered, we lose not just that client but the entire consulting category |
| **Decision** | Full silo. Client engagement data never enters prompts, documents, or conversations for other engagements. Anonymized insights require Natalia's review before any cross-use |
| **When this applies** | Any time you're working on one client engagement and recall something from another |

### Rule: Human Editorial Review Before Publishing

| Dimension | Assessment |
|-----------|-----------|
| **Why** | Every's editorial quality IS the brand. Our readers trust that AI-native articles about AI are not AI slop |
| **Risk** | AI-generated or AI-assisted articles published without human taste judgment — formulaic, generic, or factually wrong |
| **Likelihood** | Low — if the rule is followed. The temptation is speed: "it's good enough, let's ship it" |
| **Impact** | High — one visibly AI-sloppy article from an AI company damages builder credibility (our #1 value) |
| **Decision** | Kate's three rigor tests and Katie's AI tells detection apply to everything published. No exceptions for speed |
| **When this applies** | Every article, newsletter, social post, or public-facing communication |

---

## Transparency: How We Talk About AI Use

### Internally

AI use at Every is expected and celebrated. You don't need to hide that you used Claude to draft something or that an agent helped you debug a problem. Demo day exists specifically to showcase AI workflows -- show what you shipped, show how AI helped you ship it.

Direct is better than coy. "I used Claude Code to scaffold this, then rewrote the core logic myself" is more useful to the team than pretending you wrote everything from scratch.

### Externally

We are honest without being performative about it.

- **Proof tracks provenance.** Green highlights mean human-written. Purple means AI-assisted. This is how we show our work.
- **Articles are always human-reviewed.** Kate's three rigor tests apply to everything we publish. AI assistance is normal and expected, but final editorial judgment is always a human call. Every article must articulate something true, offer learnable value, and sound authentically like the writer.
- **We don't disclaim unnecessarily.** We don't slap "AI-assisted" labels on everything as a liability hedge. We also don't hide AI involvement. The standard is: if someone asked "did AI help with this?", we'd answer honestly and specifically. That's it.
- **AI tells are rejection criteria.** Katie Parrott built detection for formulaic transitions, hedging without substance, vague pronouns, and other signs of unedited AI output. If your writing has these, it's not ready -- regardless of whether a human or AI wrote it.

---

## Exception Process

Need to use a tool that's not on the approved list? Need to use confidential data in an AI workflow? Here's how.

### Who to Ask

| Exception Type | Ask |
|---------------|-----|
| New AI tool (engineering) | Your product GM, plus Danny or Andrey for security review |
| New AI tool (editorial) | Kate Lee |
| Confidential data use (client) | Natalia |
| Confidential data use (financial) | Dan |
| Cross-engagement data (any kind) | Natalia, and assume the answer is no unless she says otherwise |

### What to Include in Your Request

1. **What you want to do** -- specific tool, specific data, specific purpose.
2. **Why the approved tools don't cover this** -- what gap exists.
3. **What data is involved** -- be precise. "Some client stuff" is not precise.
4. **What could go wrong** -- demonstrate you've thought about the risk.
5. **How you'd mitigate it** -- what safeguards you'd put in place.

### Response Time

Expect a same-day response for urgent requests via Slack. Non-urgent requests should go through normal async channels and expect 24-48 hours.

### If You're Not Sure Whether You Need an Exception

Ask anyway. A 30-second Slack message is always cheaper than a confidentiality breach. Nobody will think less of you for checking.

---

## Quick Reference

For the busy days when you need the rules in ten seconds:

1. **Use approved tools.** They're listed above.
2. **Public data goes anywhere approved.** Internal data stays in approved tools.
3. **Confidential data needs explicit permission.** Ask Natalia (client) or Dan (financial).
4. **Client data never crosses engagements.** Full stop.
5. **AI use is celebrated, not hidden.** Show your work at demo day.
6. **Final editorial judgment is always human.** AI drafts, humans decide.
7. **When in doubt, ask.** It's always the right call.

---

## Review & Updates

This policy is reviewed quarterly. Changes require Dan + the relevant domain lead (Kate for editorial, Natalia for consulting/client data).

| Version | Date | Changes | Approved By |
|---------|------|---------|-------------|
| v1.0 | 2026-04-01 | Initial policy | Dan Shipper, Kate Lee, Natalia Quintero |

**Previous version:** First version
**Next scheduled review:** 2026-07-01

If you hit a situation these rules don't cover, or if a rule creates friction that doesn't match the actual risk, say something. Bring it to Dan or Brandon. Patterns of friction (three or more logged instances) trigger a formal review through the governance learning loop.

We'd rather update the policy than have people quietly ignore it.

*Questions? Ask in #engineering-learnings or DM the relevant approver directly.*
