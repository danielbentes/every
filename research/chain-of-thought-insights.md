---
title: Chain of Thought Insights
layout: default
parent: Reference
nav_order: 2
---

# Chain of Thought Insights: Dan Shipper's Articles on Every.to

Extracted from Dan Shipper's Chain of Thought column at Every.to. Dan Shipper is CEO and cofounder of Every.

---

## 1. The Two-Slice Team
**Published:** February 13, 2026 (Updated March 10, 2026)

**Summary:** Dan Shipper argues that Amazon's "two-pizza rule" (teams of ~10 people) is obsolete. With modern AI, the optimal unit is the "two-slice team"---a single person operating as a product leader. Every runs 4 software products, each led by one person, with 20 full-time employees total and 99% of code written by AI agents.

### Organizational Insights
- Every has 4 software products, each run by a single person, and 6 business units total
- 20 full-time employees across the company
- 99% of code is written by AI agents
- **Monologue** (smart dictation app): Led by Naveen Naidu. 30,000 daily transcriptions, 1.5 million words transcribed daily, 143,000 lines of code. Naveen wrote nearly all code himself using Codex and Opus. AI assists with customer service, market research, business strategy, and product decisions.
- **Spiral** (AI writing helper): Content repurposing tool
- **Cora** (AI email assistant): Led by Kieran Klaasen. Processes millions of emails daily. Employs an external senior full-stack engineer (part-time). AI handles infrastructure challenges too complex for single-pass model solutions.
- **Proof** (agent-native markdown editor): Built by Dan Shipper in spare time. Enables human-AI collaboration on markdown documents. Tracks authorship/provenance. Traditionally would require 3-4 engineers for 6 months. Available to paid Every subscribers.

### Team Structure: Internal Agencies
- Rather than adding full-time staff to products, two-slice teams pull from flexible shared resources
- **Design team**: Led by Lucas Crespo, 3 people
- **Growth team** and **Marketing team** also serve as internal agencies
- Team members rotate across projects (e.g., a designer works on Monologue UI one week, Spiral promo banner the next, Cora templates simultaneously)
- External specialized freelancers brought in for specific challenges

### Values/Philosophy
- Speed, autonomy, and variety are the three key advantages of this model
- Single leaders can accomplish work typically requiring 3-4 people pre-AI
- AI enables rapid onboarding without requiring product leaders to context-switch
- The model depends entirely on modern AI capabilities

### Key Quotes
- The company functions as a coordinated "two-pizza company" through shared resources, understanding, and coordination mechanisms (observation from commenter Michael Fisher)

---

## 2. Compound Engineering: How Every Codes With Agents
**Published:** December 11, 2025

**Summary:** "Compound engineering" is Every's four-step process where AI agents handle code generation while human engineers orchestrate and learn. The methodology challenges assumptions that coding is inherently difficult and engineers are scarce resources. A single developer can do the work of five developers from a few years ago.

### Organizational Insights
- Every operates five in-house software products, each managed by a single person: Cora, Spiral, Sparkle (Mac file organization), Monologue
- Products serve thousands of daily users for substantive work---not prototypes

### The Four-Step Compound Engineering Loop
1. **Plan (80% of developer time):** Agents research the codebase and commit history. Agents survey the internet for best practices. Output: detailed implementation plan documenting objectives, proposed architecture, specific code approaches, research sources, and success criteria. Purpose: build shared mental model between developer and agent.
2. **Work (20% of developer effort):** Agent transforms plan into task list and builds incrementally. Uses model context protocols (Playwright, XcodeBuildMCP) enabling agents to simulate user interaction during development. Agent iterates on code, observes issues, and self-corrects.
3. **Assess:** Traditional tools (linters, unit tests, manual testing). Automated code review agents examine work from multiple perspectives. Their compound engineering plugin deploys 12 parallel subagents checking security, performance, complexity, and bloat. Developer decides which findings require fixes.
4. **Compound (the core innovation):** Document learnings---bugs, performance issues, problem-solving approaches. Store as prompts within codebase or plugins. Automatically distributes knowledge to entire team. New hires access institutional memory without onboarding delays.

### Tools Used
- Claude Code (primary)
- Factory's Droid
- OpenAI's Codex CLI
- Custom compound engineering plugin for Claude Code

### Values/Philosophy
- Planning is 80% of the work; execution is 20%
- Knowledge should compound across teams through automated documentation
- Traditional hiring signals (offline coding assessments) are obsolete
- Multi-week new hire ramp periods are eliminated
- Technology lock-in due to legacy code complexity is reduced

### Key Quotes
- "A single developer can do the work of five developers from a few years ago"

---

## 3. The Knowledge Economy Is Over. Welcome to the Allocation Economy.
**Published:** January 18, 2024 (Updated March 24, 2026)

**Summary:** AI transforms the economy from knowledge-based to allocation-based. In the age of AI, every maker becomes a manager. The skills that matter shift from "what you know" to how you allocate AI resources---vision, taste, quality evaluation, and project management.

### Organizational Insights
- ChatGPT changed Shipper's understanding of work: summarizing information was an invisible skill bundled into "intelligence." Now AI handles summarization, and intelligence "learns to be the thing that directs or edits summarizing, rather than doing the summarizing myself"
- Only approximately 1 million U.S. managers (12% of workforce) currently develop allocation skills
- Even junior employees will be expected to use AI, forcing them into the role of "model manager"

### Values/Philosophy
- The knowledge economy rewarded "what you know and your ability to bring it to bear in any given circumstance." With AI matching human knowledge retrieval, this advantage disappears.
- AI is "an abstraction layer over lower-level thinking" (Evan Armstrong's framework)
- Critical management competencies for the allocation economy: vision and taste development, work quality evaluation, resource direction capability, project timeline estimation

### Key Quotes
- "In the age of AI, every maker becomes a manager."

---

## 4. Why Generalists Own the Future
**Published:** September 6, 2024 (Updated February 21, 2026)

**Summary:** Generalists possess a critical advantage in the AI era. Their true strength is not shallow breadth of knowledge but the ability to adapt to new situations, formulate the right questions, and operate in uncertain ("wicked") environments where rules are unclear and feedback is delayed.

### Organizational Insights
- Generalists are characterized as curious professionals who move across domains, enjoy problem-solving in uncertain areas, and excel at combining diverse knowledge for novel challenges
- LLMs are proficient in "kind" environments (immediate feedback, clear repetitive patterns) but limited in novel problem-solving
- The competitive advantage of generalists centers on question formulation rather than immediate answers

### Values/Philosophy
- "Measuring [generalists] against their rudimentary coding abilities or their working knowledge of French baking technique misses their true advantage: the ability to adapt to new situations"
- References David Epstein's *Range*: distinguishes "wicked" environments (where generalists thrive) from "kind" environments (where specialists and LLMs excel)
- Generalists identify problems specialists may overlook entirely

---

## 5. Working Right at the Ragged Edge of AI
**Published:** May 24, 2024 (Updated January 30, 2026)

**Summary:** An interview with Microsoft CTO Kevin Scott about building enduring businesses in the AI era. Scott was the first person at Microsoft to recognize the importance of AI and instigated its OpenAI partnership. (Note: Most content behind paywall.)

### Organizational Insights
- Kevin Scott was "the first person at Microsoft to recognize the importance of AI and instigated its OpenAI partnership, which has become the single most important strategic move at Microsoft since the dot-com era"
- Scott expressed optimism that "in the next two to three years, a model will exist that can synthesize a Kevin Scott, and virtual Kevin can go be CTO of Microsoft"

### Values/Philosophy
- Building at the edge of AI capabilities means embracing uncertainty and rapid capability shifts

---

## 6. When AI Gets More Capable, What Will Humans Do?
**Published:** June 28, 2024 (Updated February 5, 2026)

**Summary:** Introduces "capability blindness"---humanity's tendency to assume technological stasis despite rapid progress. As AI becomes more capable, humans shift from "sculptors" (directly creating work) to "gardeners" (managing conditions for AI output). What remains valuable: original research, original long-form thinking, audience acquisition, and consistency.

### Organizational Insights
- Claude 3 Opus significantly outperforms GPT-4 in voice replication and content adaptation
- "Claude mostly wrote this tweet...though I edited it"
- Claude struggles with original long-form content because "complexity scales superlinearly with the length of a piece of text"
- Every's development of Spiral reflects the strategy of building tools for AI-assisted content adaptation
- Every has a consulting practice "focused on helping mid-to-large-sized organizations implement AI and train their workforce to adopt it"

### What Remains Valuable in AI-Generated Content World
1. **Original Research:** "Uncovering new facts is still going to be valuable. Writing them will be much more of a commodity."
2. **Original Thinking (Long-form):** Content requiring genuine original thought outside well-defined formats
3. **Audience Acquisition:** "More and more power will accrue in those companies that have novel acquisition methods that do not rely on any gatekeeper" (Evan Armstrong)
4. **Consistency:** Sustained publishing builds mindshare

### Values/Philosophy
- The gardener metaphor: a gardener doesn't grow plants directly but "sets up the conditions for the garden to grow." Humans become "model managers" who establish optimal conditions for AI output, then selectively apply direct human skill ("sculpting") when it genuinely matters.
- Warns against "capability blindness"---dismissing AI progress based on past failures
- Cites Ross Douthat's 2012 prediction that Facebook couldn't monetize (proven spectacularly wrong by Meta's $134B revenue in 2023)

---

## 7. The Magic Minimum for AI Agents
**Published:** July 15, 2025 (Updated March 26, 2026)

**Summary:** Introduces "the magic minimum"---a new business viability metric for AI agents that challenges the traditional "toothbrush test" (products used twice daily). AI agents can build billion-dollar businesses through periodic high-value interventions rather than daily engagement, because proactive agents don't need users to remember to open them.

### Organizational Insights
- Every implemented an internal version of Spiral (agentic ghostwriter) in their Discord server
- The agent reads daily channel conversations and proactively pings Shipper with tweet pitch ideas derived from internal discussions
- **Sparkle** (file management) runs background Mac organization; users rarely open it directly
- The "allocation economy" creates expanded opportunities for specialized tools previously limited by human memory constraints

### Values/Philosophy
- Proactive agents fundamentally alter software economics: "they'll be able to work on their own and pop up when they've done something valuable"
- Before AI, users defaulted to feature-rich platforms like Notion/Excel over specialized occasional-use tools simply because they forgot specialized alternatives existed
- Professional services analogy: therapists, dentists, accountants maintain relationships through periodic contact and proactive outreach, not daily interaction

### Specific Team/Workflow Details
- Every offers: AI training, adoption consulting, plus tools (Spiral, Sparkle, Cora, Monologue) bundled in subscription model

---

## 8. Agent-Native Architectures: How to Build Apps After the End of Code
**Published:** January 9, 2026 (Updated February 17, 2026)

**Summary:** Contrasts traditional software architecture (skyscrapers---precise, load-tested, brittle) with agent-native architecture (gardens---organic, growing, adaptive). Agent-native apps have an AI agent as the core rather than code, with features defined by prompts naming desired outcomes rather than procedural steps. Every pivoted its whole software strategy around this paradigm.

### Organizational Insights
- Every "pivoted our whole software strategy" around agent-native architectures
- The company published: a comprehensive guide to agent-native architectures, a skill module for a compound engineering plugin for Claude Code, and supporting documentation
- Agent-native architecture: "the core is an agent---something squishy and alive, planted in sun and soil"
- These apps are described as "Claude Code in a trenchcoat"

### Values/Philosophy
- "Developers only have to name the what" while the agent handles the how
- Users can modify app behavior through natural language
- This approach "levels the playing field of power"---democratizing software creation
- Traditional software's control paradigm is questioned: "How can we allow software so much freedom?"
- Future generations might view precise, controlled skyscraper-era software "wistfully" as "a gorgeous, elaborate attempt to impose total control on a world that doesn't want to be controlled"

### Decision Details
- Pivoting entire software strategy to agent-native was a company-wide strategic decision
- Resources published: every.to/guides/agent-native

---

## 9. How I Built Spiral
**Published:** July 26, 2024 (Updated January 14, 2026)

**Summary:** Documents Dan Shipper's experience building Spiral, a prompt builder tool, through collaborative development with Claude (Anthropic's AI). The article serves as a behind-the-scenes narrative of this building process. (Detailed methodology behind paywall.)

### Organizational Insights
- Spiral is positioned as a prompt builder tool
- Built through AI-assisted development (collaborative process between Shipper and Claude)
- Part of Every's product suite alongside Sparkle, Cora, and Monologue
- The complete chat conversation between Shipper and Claude used to develop Spiral's original code is available to paying subscribers

### Values/Philosophy
- CEO personally builds products using AI coding tools
- Demonstrates the "builder CEO" philosophy where leadership involves hands-on product development

---

## 10. AI Can Do My Email Now
**Published:** June 30, 2023 (Updated February 4, 2026)

**Summary:** A personal review of Superhuman's AI beta features for email management. Shipper explores how AI tools address his tendency to overwrite verbose, carefully-crafted email responses. Praises Superhuman's restrained, invisible-by-default approach to AI integration.

### Organizational Insights
- Shipper's email writing style: tendency to overwrite with excessive consideration, "lots of exclamation points and smiley faces," covers "every corner case" when replying
- He frames one-line emails as demonstrating confidence, command, and psychological detachment

### Values/Philosophy (on Product Design)
- Praises Superhuman's design philosophy of making AI "totally invisible unless I snap my fingers"
- Good AI integration is non-intrusive and prevents AI from becoming "messy and chaotic" in the user interface
- Restraint in AI feature design is a virtue

---

## 11. We're Building AI Into Our Media Business
**Published:** May 5, 2023 (Updated January 14, 2026)

**Summary:** Every's comprehensive strategy for integrating AI into its media business. Covers four predicted AI-driven media transformations: de-risked content automation, unbundling research from narrative, unlocking unwritten stories, and human-AI collaborative creative work. Includes concrete operational examples of how Every already uses AI.

### Organizational Insights
- Every's founding mission: "create more high-quality business writing in the world"
- Co-founder Nathan built Lex.page, an AI writing app
- Every built chatbots enabling readers to question written content

#### The Digest Summarization Project
- Lucas Crespo (manages ad and course operations) built an automated summarization tool in Python deployed on Heroku within two days despite having zero prior programming experience
- He used GPT-4 to create the application by describing requirements and requesting help when encountering obstacles
- Workflow: input headline, author, and article text to generate summaries modeled on Every's previous Digest summaries
- Shipper still dedicates time editing summaries, occasionally rewriting when quality falls short

### Four Predicted AI-Driven Media Transformations

1. **De-Risked Content Automation:** Seven de-risking strategies become easier for AI: summarizing others' work, content arbitrage, format structures, shorter content, beat-focused reporting, sequels/remixes, interview-based content
2. **Unbundling Research from Narrative:** Expose underlying transcripts, searches, editorial conversations through chatbots; let readers interrogate source material and request customized story versions
3. **Unwritten Stories Becoming Published:** "The best ideas in business are never written down---they're locked up in people's heads." AI enables converting transcripts into polished pieces, enabling "the dramatic expansion of the number of high-quality posts we can publish from people who don't consider themselves writers but who have incredible ideas about business"
4. **Human-AI Collaborative Creative Work:** AI won't eliminate writers but will reshape required skills. Technologies grant humans additional time for "satisfying creative work at a higher level of ambition and scale" while making media businesses "significantly easier to run predictably"

### Values/Philosophy
- "The best way to think about things like this is to experiment"
- Hands-on experimentation over theoretical resistance to AI
- Quality matters: GPT-4's summarizations "still lack the _zing_ and voice of truly great human writing"
- Great writing---even de-risked formats---remains "a complex activity where what it means to be 'good' is changing all of the time"
- Human oversight remains essential "for the foreseeable future"
- On Hollywood AI fears: "it's right to be hopeful that Hollywood and its screenwriters can find an equilibrium that uses AI to augment writers and compensate them better---rather than ban it entirely"

---

## 12. A Few Things I Believe About AI
**Published:** April 20, 2023 (Updated January 25, 2026)

**Summary:** Four core beliefs about AI after 6 months of intensive engagement. Knowledge orchestration is the primary bottleneck. End-to-end interaction data drives model improvement. Startups integrating entire processes will dominate. AI will progress where traditional science has struggled.

### Organizational Insights

#### Belief 1: Knowledge Orchestration is the Primary Bottleneck
- GPT-4 is "quite good at reasoning" but constrained by ability to provide relevant knowledge at the right time
- Three operational layers: foundational model layer (context windows), developer tools/infrastructure (LlamaIndex, Langchain), vector databases (Pinecone, Weaviate, Chroma)

#### Belief 2: End-to-End Interaction Data Drives Model Improvement
- Valuable knowledge includes "end-to-end interaction data about the lifecycle of any process"---visible beginning, middle iterations, and measurable results
- Enables RLHF and fine-tuning

#### Belief 3: Startups Integrating Entire Processes Will Dominate
- "Startups that are horizontally integrated over a process will be dominant"
- More process visibility enables better improvement
- Horizontal integration means "replacing things that their customers are paying other companies for with their own solution---so they can see more of the process and integrate it together"
- Examples: Replit (idea-to-software in browser), OpenAI/ChatGPT (API to direct consumer), Midjourney (generation to editing to social), Adobe Firefly
- Andrej Karpathy: the internet contains primarily "final" text; "all of that 'latent structure' of your drafts, edits, going back and forth etc. is sadly lost"---this missing iteration data is "ideal data for GPTs"
- Incumbents face privacy concerns and internal political resistance when sharing data across ecosystem products; startups built for process integration have structural advantages

#### Belief 4: AI Will Progress Where Science Has Struggled
- AI enables predictions in domains where simple causal scientific explanations remain elusive: psychology, social sciences, economics
- Cancer screening and anxiety/depression prediction without requiring complete scientific understanding

### Values/Philosophy
- Adopting "a 10,000 foot perspective" amid rapid iteration cycles
- Describes the pace as having "a SpaceX rocket strapped to my butt" while "you constantly feel behind"

---

## 13. Capability Blindness and the Future of Creativity
**Published:** April 12, 2024 (Updated December 17, 2025)

**Summary:** Introduces "capability blindness"---a cognitive bias where people fail to recognize improvements in technology because they're jaded by previous experiences. Demonstrates Claude 3 Opus's writing capabilities at 70-80% voice accuracy. Poses the question: "What's rare in a world with infinite good writing?" (Partially paywalled.)

### Organizational Insights
- Claude 3 Opus can capture a writer's voice at 70-80% accuracy with proper prompting
- Shipper generated a tweet using Claude with examples from his podcast transcripts and tweets
- "Claude mostly wrote this tweet...though I edited it"
- Genuine capability leap between GPT-4 and Claude 3 Opus

### Values/Philosophy
- Capability blindness: people assume the world remains static rather than continuously evolving
- Historical precedent: Ross Douthat's 2012 NYT analysis declared Facebook unprofitable---by 2023, Meta achieved $134B revenue
- The subtitle "We used to be sculptors. We're all about to be gardeners" captures the transition from direct creation to condition-setting

---

## 14. The Great AI Unbundling
**Published:** August 1, 2024 (Updated February 7, 2026)

**Summary:** General-purpose AI chatbots will generate startup opportunities just as Excel spawned the B2B SaaS era. ChatGPT and Claude increase demand for "wrappers" as users discover use cases general tools aren't designed for. Spiral is presented as a case study of this unbundling pattern.

### Organizational Insights
- Spiral launched approximately one month before publication, already achieving "more than 3,500 users and is growing every day"
- Spiral automates "repetitive creative work like X posts, LinkedIn posts, headline creation, and product release notes"
- Spiral uses Claude as its backend, but Claude's chat interface lacks optimization for Spiral's specific workflows (maintaining complex prompts, team prompt-sharing)
- Every's ecosystem: Chain of Thought column, AI & I podcast, software (Monologue, Sparkle, Spiral, Cora), subscription model, community of 100,000+ users described as "leaders, builders, and innovators"

### Values/Philosophy
- Challenges the pejorative connotation of "AI wrapper" applications: "ChatGPT and Claude are great places to find startup ideas"
- The three-phase unbundling pattern: (1) general-purpose tool adoption, (2) discovery of niche workflow inefficiencies, (3) purpose-built application creation
- Startup ideation framework: "If you want to build a startup in the AI era, just watch how you use ChatGPT or Claude. If you're doing something repeatedly---and the outputs are impressive---there's a chance it could be its own app"
- Excel unbundled into Asana, Looker, QuickBooks over 15 years---AI chatbots will follow the same pattern

---

## 15. Five New Thinking Styles for Working With Thinking Machines
**Published:** October 10, 2024 (Updated March 26, 2026)

**Summary:** AI requires fundamentally different cognitive approaches than traditional scientific thinking. Western culture defaults to scientific/rationalist frameworks, but "thinking machines" demand new intellectual methodologies. The article introduces at least two of five new thinking styles. (Partially paywalled.)

### Organizational Insights
- References Andrej Karpathy's "Software 1.0" (human-written instructions/scientific thinking) vs. "Software 2.0" (trained models searching solution spaces/engineering thinking)
- The subtitle: "AI is turning science into engineering---with unprecedented changes for how we see the world"

### Two of Five Thinking Styles Revealed
1. **Essences vs. Sequences:** Pre-AI approach emphasized identifying core elements and building forward. New approach: identify sequential patterns in behavioral data without predetermined definitions (e.g., SaaS churn prediction from 100 days of user behavior vs. explicit rule-based churn indicators)
2. **Rules vs. Patterns:** Pre-AI software required encoding explicit task definitions. New approach: provide mood boards or high-level behavioral descriptions, let AI extract underlying patterns and generate rulesets

### Values/Philosophy
- The shift from rule-based to pattern-based thinking is fundamental
- Teams can now describe creative intent rather than specifying precise rules

---

## 16. Seeing Like a Language Model
**Published:** October 3, 2025

**Summary:** Language models reveal a fundamental shift from the Western rationalist worldview (logic, documentation, universal truth, simplicity) to a new pattern-based worldview (interconnection, context-dependence, correlation, paradox). Part of Shipper's book project about the worldview developed by "writing, coding, and living with AI."

### Organizational Insights
- Part of Shipper's book project about AI worldview

### The Old Western Worldview (Five Assumptions)
1. Logical clarity solves any problem
2. Explicit documentation enables understanding
3. Truth is universal regardless of context
4. Logic cannot contradict itself
5. Simplicity indicates truth

### The New Worldview Framework
- **Reality as Web, Not Chain:** Interconnected relationships, not linear cause-effect
- **Meaning Through Contrast:** "Dark" means differently in "dark chocolate" vs. "dark thoughts"
- **Incomplete Explanations:** "When everything is connected to everything else, any attempt to explain one thing requires explaining everything"
- **Correlation Over Causation:** Complex systems resist if-then reduction
- **Context as Essential:** Context shapes meaning fundamentally, not noise to filter
- **Participatory Knowledge:** Observer perspective shapes observed reality
- **Pluralism Over Monotheism:** Multiple frameworks capture different aspects; no single theory explains everything
- **Embracing Paradox:** Uncertainty as creative force, not obstacle

### Values/Philosophy
- "Our tools change how we see the world...now we've built new tools---language models---that can work with what previously only our intuition could handle"
- "If you believe that the world is composed of atoms rather than spirit...it's because of this style of thinking"
- The symbolic AI failure (trying to encode intelligence through formal rules) mirrors the limits of the Western worldview

---

## 17. Seeing Business Like a Language Model
**Published:** October 17, 2025 (Updated February 5, 2026)

**Summary:** Business principles function as useful heuristics rather than universal laws. Disruption theory, Porter's Five Forces, and jobs-to-be-done analysis operate as situational patterns, not scientific axioms. Language models' "next-token prediction" methodology offers superior business intuition versus rigid principle application.

### Organizational Insights
- Part of Shipper's book series on AI worldview
- Shipper is developing a worldview through "writing, coding, and living with AI"

### Why Business "Laws" Fail
- **Equifinality and Multifinality:** Multiple paths to identical outcomes; identical paths producing divergent results (Apple iPhone disrupted from the high end, contradicting disruption theory; Netflix competed directly with Blockbuster's core)
- **Lack of Controlled Experiments:** "What you choose to test is significantly more important than which test wins." Strategic decisions cannot be A/B tested.
- **Sensitive Dependence on Initial Conditions:** Butterfly effects---changing any variable in Netflix's rise alters results entirely
- **Hidden Exceptions and Subjectivity:** Conditions enabling principles cannot be fully specified in advance. Customer research lacks objectivity.

### Values/Philosophy
- "Business principles work---until they don't"
- "Business 'laws' are more like patterns or tendencies that we observe, but they don't have the same predictive power or universal applicability" as physical laws
- Memorizing frameworks doesn't generate application instincts when situations demand them
- The solution: build "gut-level next token prediction" rather than treating business maxims as universal rules
- Pattern recognition and tacit knowledge transcend explicit principles

---

## 18. Seeing Science Like a Language Model
**Published:** October 10, 2025 (Updated January 12, 2026)

**Summary:** Second piece in Shipper's book series. Argues that language models reveal what centuries of scientific method missed: some truths resist reduction. Uses the psychology replication crisis as a case study for the limits of reductionist scientific thinking. (Partially paywalled.)

### Organizational Insights
- Written from Bocas Del Toro, Panama, from "a little cabin in the jungle at the top of a hill five minutes from the Caribbean sea"
- Part of Shipper's book project: "I'm writing a book about the worldview I've developed by writing, coding, and living with AI"

### Key Arguments
- "The way things appear is different from the way they are---we trust the science"
- Enlightenment physics concepts permeate modern language: "forces" shaping society, "momentum" in markets, "chemistry" with people, "orbit," "leverage," "friction"
- "This way of thinking has also begun to reach its limits. Just as it did with machine learning research, the tendency to reduce, to break apart, to make explicit, and to generalize has failed, hard, in many places"
- Psychology's replication crisis: "Scientists use tools built for physics to make their intuitive theories fit into statistical models, only to find that their results can't be reproduced"
- The issue is "not necessarily a crisis of replication but one of generalizability" (psychologist Tan Yarkoni): we overstate how universal findings are

### Values/Philosophy
- "That we see the world the way we do is a testament to how powerfully ideas shape what we see, and our capacity, through cultural transmission, to know things that we have not directly experienced"
- References David Deutsch's "hard-to-vary" explanations as the currency of science
- The subtitle: "Language models reveal what centuries of scientific method missed: Some truths resist reduction"

---

## 19. Seeing Creativity Like a Language Model
**Published:** October 24, 2025 (Updated February 6, 2026)

**Summary:** Fourth piece in the book series. AI reshapes creative work by elevating creators to allocation roles---from "sculpting to gardening." Includes deeply personal account of Shipper's 2023 organizational crisis and reorientation. Presents six concrete AI applications for creative work and argues AI enables a return to Athenian generalism.

### Organizational Insights

#### Personal Crisis and Organizational Restructuring (2023)
- Every faced stagnant growth, departed co-founder, personal identity crisis between entrepreneurship and writing
- Shipper queried GPT-3: "writers who also have great businesses"
- System surfaced role models: Sam Harris, Bill Simmons, Ezra Klein, Nate Silver, John Green
- **Restructuring decision:** Made writing the first half of each workday non-negotiable. Hired talented executives to handle operations.
- **Result:** "The business subsequently took off in a way that it never had before"

#### The "Ineffable List" System
- Shipper maintains a phone note documenting moments that resonate---quotes, observations, scenes
- Examples: nephew's question "Where does the wind go?", Chekhov excerpt, family cemetery business process ("The System")
- Functions as personal training data for creative work

#### Six AI Applications for Creative Work
1. **Understanding dense material:** ChatGPT with image capture and voice mode to translate philosophy, ML texts, literature
2. **Extracting ideas faster:** Voice dictation converts mental "potential energy" into linear text
3. **Rapid summarization:** AI generates foundational summaries (half-day research to seconds), leaving refinement to taste
4. **Multi-perspective editing:** AI simulates various editorial voices; aggregates reader feedback using tools like Rally
5. **Cross-platform adaptation:** Long-form to social media versions, thumbnails, headlines for X, LinkedIn, YouTube
6. **Prototype construction without capital:** Spiral built in days rather than months, no investor funding needed

### The Allocation Economy Framework (Expanded)
- Required skills: vision and taste in ideas and language, effective communication of intent, project planning and timeline estimation, task distribution among specialists, strategic micromanagement for detail quality
- "These are the skills of human managers"---showrunners, directors, conductors operate identically
- Currently only ~10% of workforce fills these roles; future requires universal adoption

### Historical Arc: Generalism
- **Ancient Athens:** Citizen generalists (farmer, lawyer, juror, warrior simultaneously); cultural golden age
- **Specialization era:** Adam Smith's pin factory increased productivity 2,400x (20 to 48,000 pins/day) through division of labor
- **Cost:** Karl Marx's alienation; Henry Ford's assembly line workers quit despite doubling pay
- **AI as Resolution:** AI provides "effectively a thousand PhD-level experts in your pocket," enabling return to Athenian generalism without sacrificing depth

### Values/Philosophy
- "If I was really honest with myself, I actually wanted to be a writer"
- AI-generated art concerns: contests the rationalist view that art equals "text on page or pixels in image---completely divorced from context and history." Counter: context is determinative.
- Cultural taboo around AI art signals fertile creative ground for "brave creatives who embrace it to produce novel works"
- "You need vision, a taste for ideas and for language, and an ability to effectively communicate what you want"
- "AI can enable us to expand our creative and professional repertoire, breaking free from narrow specialization"

---

## 20. Admitting What Is Obvious
**Published:** September 8, 2023 (Updated January 13, 2026)

**Summary:** A deeply personal essay about how people suppress obvious truths about themselves due to internalized expectations. Shipper reveals that he founded Every partly as a mechanism to pursue writing while maintaining founder credibility, and that admitting "I actually wanted to be a writer" was the turning point.

### Organizational Insights
- Shipper previously sold a B2B software business before founding Every
- Initially described himself as a "founder who also liked to write" rather than admitting his primary identity
- Writing was his greatest passion despite enjoying most startup responsibilities (coding, sales, marketing, managing, fundraising)
- Every functions structurally as a startup (permitting founder status) while functionally enabling Shipper's authentic professional identity as a writer

### Values/Philosophy
- References Robert Bly's "invisible bag" concept: people carry rejected parts of themselves since childhood
- The bag accumulates authentic desires deemed unacceptable by parents, teachers, peers
- Admitting obvious truths feels terrifying because it appears to threaten professional identity, ability to build consequential companies, career earning potential
- The path to freedom: acknowledging what you already know about yourself despite potential consequences

### Key Quotes
- Shipper realized "writing was his greatest passion" but had suppressed this truth
- Every was created partly so he could write while maintaining the identity of a founder/entrepreneur

---

# Cross-Cutting Themes

## How Dan Shipper Thinks About Running Every

### Company Structure
- 20 full-time employees, 6 business units, 4 software products each run by 1 person
- 99% of code written by AI agents
- Internal agency model: design (3 people, led by Lucas Crespo), growth, marketing teams rotate across products
- External freelancers for specialized challenges
- 100,000+ community members

### Products
- **Spiral:** AI writing/content repurposing tool (agentic ghostwriter), 3,500+ users at launch
- **Cora:** AI email assistant, processes millions of emails daily
- **Monologue:** Smart dictation, 30K daily transcriptions, 1.5M words/day
- **Sparkle:** Mac file organization, background operation
- **Proof:** Agent-native markdown editor for human-AI collaboration

### Core Philosophy
1. **Allocation over knowledge:** The future belongs to those who direct AI resources, not those who possess knowledge
2. **Generalists over specialists:** Ability to adapt, ask the right questions, and work across domains
3. **Gardening over sculpting:** Set conditions for AI output rather than doing everything directly
4. **Experimentation over theory:** "The best way to think about things like this is to experiment"
5. **Compound knowledge:** Document learnings as prompts that automatically distribute across the team
6. **Authentic identity:** Admitting what you truly want (writing) and building a company around that truth
7. **Agent-native architecture:** Software where the core is an AI agent, not code
8. **Planning dominates execution:** 80% planning, 20% building in the compound engineering loop
9. **Speed and autonomy:** Two-slice teams ship fast and pivot quickly
10. **AI wrappers are opportunities, not liabilities:** General-purpose AI creates demand for purpose-built tools

### Decision-Making Style
- Uses AI to surface patterns he already intuitively knows (GPT-3 query for "writers who also have great businesses")
- Makes writing the first half of each workday non-negotiable
- Pivots entire software strategy when paradigm shifts (agent-native architectures)
- CEO personally builds products (Proof built in spare time)
- Hires talented executives to handle operations so he can focus on writing and product

### Evolution of Every
- Founded as media business to "create more high-quality business writing in the world"
- Co-founder Nathan departed; Shipper faced stagnant growth and identity crisis (2023)
- Restructured: writing first, hired executives for operations
- Business "took off in a way that it never had before"
- Expanded into AI software products (Spiral, Cora, Monologue, Sparkle, Proof)
- Added consulting practice for mid-to-large organizations
- Pivoted software strategy to agent-native architectures (2026)
- Developed compound engineering methodology for AI-first development
