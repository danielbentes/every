---
title: "Quality Standards by Output Type"
layout: default
parent: Genome
nav_order: 7
---

# Quality Standards by Output Type

## Newsletter Articles

### What "Good" Looks Like
- Has a specific, falsifiable thesis — not a recap, but an argument
- Grounded in first-hand experience ("I built this," "We tried this," "Here's what happened")
- Uses concrete examples with specific names, numbers, and tools
- Sounds authentically like the author — not interchangeable with any other writer
- Offers a framework, technique, or insight the reader can apply immediately
- Written in first person with conversational tone
- References specific AI tools by name with real screenshots/examples when relevant

### Pass Criteria
1. Passes all three rigor tests: (a) articulates something true, (b) offers learnable value, (c) sounds authentically like the writer
2. Free of AI tells: no formulaic transitions ("Moreover," "Furthermore"), no hedging ("It's worth noting"), no vague pronouns, no correlative constructions that add nothing
3. Has a clear thesis stated in the first 3 paragraphs
4. Contains at least one concrete example from real experience
5. Would make someone forward it to a colleague with "you need to read this"

### Anti-Patterns (What's Not Acceptable)
- News recap without a point of view: "Here's what happened in AI this week" with no thesis
- Corporate blog voice: "We're excited to announce our latest innovation in..."
- Theory without practice: abstract frameworks not grounded in real experience
- AI slop: formulaic structure, hedging language, generic advice that could apply to anything
- "Content marketing disguised as insight" — promotional material wearing editorial clothing

### Example: Good
> "The Knowledge Economy Is Over. Welcome to the Allocation Economy." — Makes a specific claim (AI transforms every maker into a manager), backs it with Dan's experience running Every, offers a framework (allocation skills) readers can apply immediately. Went viral because it named what people felt but couldn't articulate.

### Example: Not Acceptable
> An article that accurately summarizes recent AI model releases with benchmark comparisons but has no thesis about what it means for how readers work. Well-researched, well-written, factually correct — but reads like a recap, not an argument.

---

## Software Code (Compound Engineering Output)

### What "Good" Looks Like
- Core user flow works end-to-end
- Passes all 14 review agent checks (security, performance, architecture, data integrity, complexity, bloat, etc.)
- Includes compound artifacts: docs/solutions/ entries, CLAUDE.md updates, reusable patterns extracted
- Tests pass (unit, integration as applicable)
- Follows existing codebase patterns and conventions
- Leaves the system smarter for next time (the meta-game)

### Pass Criteria
1. All review agents report P1 findings resolved (P2/P3 at GM's discretion)
2. Tests pass
3. At least one compound artifact produced (docs/solutions/ entry, CLAUDE.md update, or reusable pattern)
4. No regression in existing functionality
5. Plan was followed or deviations are documented

### Anti-Patterns (What's Not Acceptable)
- "Works but doesn't compound" — feature ships but leaves no institutional knowledge. No docs, no patterns, no CLAUDE.md updates. Next similar feature starts from scratch.
- Ignoring review agent findings — shipping without addressing P1 findings from any of the 14 review agents
- "Vibe coding" — jumping straight to code without a plan. Plans are the primary artifact, not code.
- Over-engineering for hypothetical futures — building abstractions for requirements that don't exist yet
- Breaking existing user flows to add new features

### Example: Good
> Kieran's compound engineering feature for Cora: detailed plan in GitHub, agent executed plan in worktrees, 14 agents reviewed in parallel, fix applied before Kieran even saw it, new docs/solutions/ entry created, CLAUDE.md updated with the pattern. Next similar feature: 50% faster.

### Example: Not Acceptable
> A feature that works but was built by "vibe coding" — no plan, no review, no compound step. The feature ships, users are happy, but the system didn't learn. Next feature takes the same effort.

---

## Consulting Deliverables

### What "Good" Looks Like
- Grounded in Every's own experience ("Here's how we do this internally")
- Tailored to client's specific industry, team size, and AI maturity level
- Actionable within the client's constraints — not aspirational, practical
- Includes hands-on components (not just slides — build something together)
- Produces measurable impact (hours saved, workflows automated, capabilities unlocked)

### Pass Criteria
1. Client can implement at least one recommendation without additional help
2. Materials reference Every's actual tools and practices (builder credibility)
3. Training sessions achieve NPS >70
4. Deliverables are customized to client's vertical (finance or tech) and maturity level (L1-L4)
5. No recommendations for tools/practices Every doesn't use internally

### Anti-Patterns (What's Not Acceptable)
- Generic AI roadmap that could apply to any company: "Step 1: Identify use cases. Step 2: Build POCs."
- Recommending tools we don't use: "Consider implementing [tool we've never touched]"
- Slide-heavy, hands-off delivery: 60 slides and no hands-on building
- Overselling capabilities: promising AI can do things we haven't verified ourselves
- Breaching client confidentiality in any form — even anonymized anecdotes without permission

### Example: Good
> Hedge fund engagement: Investment analysis reduced from one week to minutes using compound engineering plugin for parallel screening. Analysts trained hands-on to build their own Claude Skills. Client can extend the system independently.

### Example: Not Acceptable
> A consulting engagement where we deliver a PowerPoint deck titled "AI Strategy Roadmap" with generic recommendations ("Adopt AI for document processing") that don't reference our actual experience or give the client anything they can implement this week.

---

## Podcast Episodes (AI & I)

### What "Good" Looks Like
- Guest has genuine expertise from building, not just observing
- Dan asks specific, curious questions — not generic interview prompts
- Conversation surfaces insights the audience can't get from reading the guest's blog
- Clear takeaway: "After listening, I will..." not just "That was interesting"
- Production quality: clean audio, tight editing, no dead air

### Pass Criteria
1. Guest has demonstrated builder credibility in their domain
2. At least 3 specific, actionable insights emerge from conversation
3. Episode is edited to remove tangents that don't serve the listener
4. Show notes include key takeaways and timestamps
5. Social clips generated capture the highest-insight moments

### Anti-Patterns (What's Not Acceptable)
- Softball interview: "Tell me about your amazing company" without challenge or depth
- Generic AI hype conversation: "AI is going to change everything" without specifics
- Guest who talks about AI but doesn't build with it (violates builder credibility by proxy)
- Poor production quality that distracts from content

---

## Social Media Posts

### What "Good" Looks Like
- Distills an article's thesis into tweet/post length without losing the argument
- Written in the author's voice, not a generic social media voice
- Specific enough to be interesting, concise enough to be shareable
- Links back to the full article for depth

### Pass Criteria
1. Captures the article's thesis (not just a teaser)
2. Sounds like the author, not like a marketing team
3. No clickbait: "You won't BELIEVE what AI did next!"
4. Includes a concrete detail or number that makes it credible

### Anti-Patterns (What's Not Acceptable)
- Corporate announcement tone: "NEW ARTICLE: 10 Ways AI Will Change Your Life!!"
- Generic motivational content: "AI is the future. Are you ready?"
- Misrepresenting the article's content for engagement
- Auto-generated social posts that clearly sound like AI (ironic for an AI company)

---

## Product Copy and Marketing

### What "Good" Looks Like
- Clear, specific value proposition in one sentence
- References what the product actually does, not what it aspires to do
- Authentic Every voice: warm, direct, slightly playful
- Includes real usage numbers when available

### Pass Criteria
1. A reader understands exactly what the product does in 10 seconds
2. Claims are grounded in actual product capabilities (not roadmap)
3. Tone matches Every voice: conversational, specific, not corporate
4. Pricing is transparent and straightforward

### Example: Good
> "Spiral: An AI writing partner with taste. $25/month. Free for Every subscribers."
> "Cora: Give AI your inbox, take back your life."
> "Monologue: 30,000 daily transcriptions. 100+ languages. Smart dictation for Mac."

### Example: Not Acceptable
> "Harness the power of AI to transform your writing workflow with our cutting-edge platform."
