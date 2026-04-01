# Organizational Anti-Patterns

Things that are technically correct but "not us." These are taste markers — the difference between generic output and output that feels like it came from Every.

## Anti-Pattern: AI Slop
- **What it looks like:** Formulaic transitions ("Moreover," "Furthermore," "In conclusion"), hedging without substance ("It's worth noting that..."), correlative constructions that add nothing ("Not only X, but also Y"), vague pronouns ("This approach," "These insights"), lists that could be in any order.
- **Why it's wrong for us:** We're an AI company that writes about AI. If our own content sounds AI-generated, we've destroyed our credibility. Our readers are sophisticated enough to spot it. Katie Parrott runs AI tells detection skills specifically to catch this.
- **What to do instead:** Write in the author's voice with specific claims, concrete examples, and natural language. If a transition is formulaic, cut it. If a sentence hedges, either commit to the claim or remove it.

## Anti-Pattern: News Recap Without Thesis
- **What it looks like:** "This week in AI: OpenAI released X, Google announced Y, Anthropic shipped Z." Accurate, timely, well-organized — and completely pointless by our standards.
- **Why it's wrong for us:** Every article needs a thesis. Our value is not in summarizing (AI does that). Our value is in interpreting — "here's what this means for how you work." Recaps are the definition of work AI has made commodity.
- **What to do instead:** Start with the thesis. "This week proved that [claim]. Here's why." Use the news as evidence for an argument, not as the content itself.

## Anti-Pattern: Corporate Blog Voice
- **What it looks like:** "We're excited to announce our latest innovation..." "At Every, we believe in the power of..." "Leverage our cutting-edge platform to transform your workflow."
- **Why it's wrong for us:** We're not a corporation. We're a group of builders who write. Corporate voice signals that no one specific is speaking, which means no one is accountable for the claim. It's the opposite of our first-person, conversational, intellectually honest voice.
- **What to do instead:** Use "I" not "we" in articles. State what you did, what happened, and what you learned. Be specific. Be personal. Be accountable.

## Anti-Pattern: Theory Without Practice
- **What it looks like:** An article or consulting deliverable that presents frameworks, models, and abstract principles without any grounding in real experience. "Organizations should consider..." without "Here's what happened when we tried..."
- **Why it's wrong for us:** Builder credibility is our ultimate value. Every recommendation, every framework, every claim must be grounded in something we or someone we know actually did. Theory without practice is management consulting, not Every.
- **What to do instead:** Always include at least one "Here's what happened when..." example. If you can't provide one, either do the thing first or clearly label the claim as speculative.

## Anti-Pattern: Code Without Compound
- **What it looks like:** A feature ships, works correctly, passes tests — but leaves no trace in the system. No docs/solutions/ entry. No CLAUDE.md update. No reusable pattern extracted. The code works but the system didn't learn.
- **Why it's wrong for us:** Compound engineering's core principle: each unit of work should make subsequent units easier. Code that works but doesn't compound is a missed opportunity — the next developer (or agent) facing a similar problem starts from zero.
- **What to do instead:** Every PR should include at least one compound artifact. Ask: "What did the system learn from this work?" If the answer is "nothing," you're not done.

## Anti-Pattern: Vibe Coding
- **What it looks like:** Jumping straight to writing code (or having an agent write code) without creating a plan first. No PRD, no research, no documented success criteria. "Let's just see what happens."
- **Why it's wrong for us:** Plans are the primary artifact at Every, not code. The compound engineering loop is Plan (40%) → Work (10%) → Review (40%) → Compound (10%). Skipping the plan means 80% of the methodology's value is lost. As Kieran says: "Plans teach the system; code just solves problems."
- **What to do instead:** Always start with a plan. Even for small tasks, write a brief plan.md that documents the objective, approach, and success criteria.

## Anti-Pattern: Consulting from PowerPoint
- **What it looks like:** Delivering consulting engagements primarily through slide decks and presentations without hands-on building. "Here's our AI strategy roadmap" as a 60-slide PDF.
- **Why it's wrong for us:** We're "builders, not followers." Our consulting clients hire us because we build things with them, not for them. A deck without a working demo, a co-built tool, or a hands-on training session is management consulting — which is exactly what we're NOT.
- **What to do instead:** Every consulting engagement should include hands-on building. Show the client something working. Let them build alongside you. The deliverable is capability transfer, not a document.

## Anti-Pattern: Over-Standardization of GM Workflows
- **What it looks like:** Mandating that all product GMs use the same tools, follow the same processes, or adopt the same AI workflow. "Everyone must use Claude Code exclusively" or "All plans must follow this exact template."
- **Why it's wrong for us:** GM autonomy is core to the two-slice team model. Yash runs parallel Claude+Codex sessions. Danny uses Droid CLI for 70% of work. Naveen lives in Linear. Kieran does plan-first development. The diversity of approaches IS a feature — it generates more institutional learning than a monoculture would.
- **What to do instead:** Share learnings across GMs (compound step), provide shared infrastructure (design team, platform), but let each GM optimize their own workflow. Standardize outputs (quality gates), not inputs (tooling choices).

## Anti-Pattern: Scaling Consulting by Diluting Practitioner Quality
- **What it looks like:** Hiring junior consultants or generic management consultants to scale the consulting practice, without ensuring they have hands-on AI building experience.
- **Why it's wrong for us:** "95% of generative AI pilots fail due to clarity problems, not technology" — Natalia Quintero. Our consulting edge is that we're practitioners who have solved these problems ourselves. Hiring people who can't build destroys that edge. One mediocre consulting engagement damages the brand more than leaving the revenue on the table.
- **What to do instead:** Only hire consultants who are themselves builders. Limit engagements to a number the team can deliver at full quality. Better to have a waitlist than to dilute.

## Anti-Pattern: Ignoring Cultural Functions When Encoding
- **What it looks like:** Automating a meeting, process, or approval chain because it has high coordination overhead, without considering whether it also serves cultural or identity functions.
- **Why it's wrong for us:** The coordination audit identified structures like demo day (HIGH cultural risk) and editorial taste discussions (MEDIUM). Encoding these without replacement creates a cultural vacuum. We've seen other companies automate standups and lose team cohesion.
- **What to do instead:** Always classify dual-system function before encoding. Encode coordination, invest in culture. If a meeting serves both, separate the functions: automate the status update, keep the human connection.
