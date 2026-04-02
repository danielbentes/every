---
title: Source Code Insights
layout: default
parent: Reference
nav_order: 8
---

# Every.to Source Code Column - Complete Insights Extraction

> Extracted from 20 articles in Every's Source Code column. Each article analyzed for organizational insights, engineering practices, workflows, tools, team structure, and operational details.

---

## 1. Compound Engineering: The Definitive Guide
**Author:** Kieran Klaassen (General Manager of Cora) | **Published:** February 9, 2026

**Summary:** A comprehensive handbook for "compound engineering," the AI-native engineering philosophy where each unit of engineering work makes subsequent units easier. Every runs all five of its products with single-person engineering teams enabled by AI assistance, inverting the traditional pattern where codebases accumulate complexity.

**Engineering Practices and Workflows:**
- Central principle: each unit of engineering work should make subsequent units easier, not harder
- Bug fixes are designed to prevent entire classes of future issues, not just the immediate problem
- Codified patterns become reusable tools that compound over time
- The system is designed to become progressively easier to understand and modify
- Pull requests function as permanent system lessons
- Code reviews update the system's defaults automatically

**Tools and Technologies:**
- Claude Code (primary AI coding tool)
- GitHub (workflow backbone, plan storage)
- Open-source compound engineering GitHub plugin for adoption

**Team Roles and Responsibilities:**
- Every operates five products using single-person engineering teams
- Kieran Klaassen is General Manager of Cora (AI email assistant)
- Products: Spiral, Cora, Sparkle, Monologue, AI&I Podcast

**Quality Control:**
- Automated code fixes applied before developer review
- Every pull request teaches the system
- Every bug becomes a permanent lesson

**Key Quotes:**
- "Each unit of engineering work should make subsequent units easier--not harder."
- "Software used to be built by armies of engineers. Now, with AI, Every runs all five of its products with single-person engineering teams."

---

## 2. Inside the AI Workflows of Every's Six Engineers
**Author:** Rhea Purohit | **Published:** October 27, 2025

**Summary:** A deep profile of all six engineers at Every, revealing how each has tailored their AI-assisted development stack to their individual working styles. The team manages four AI products, one consulting business, and a daily newsletter reaching 100,000+ readers.

**Engineering Practices and Workflows:**

*Yash Poojary (GM, Sparkle):*
- Runs Claude Code and Codex simultaneously on separate machines, comparing outputs
- Maintains a "learnings doc" capturing insights after each code push
- Mornings: focused execution only; Afternoons: exploration and experimentation
- Uses Figma MCP integration enabling Claude to read design systems directly
- Built AgentWatch (custom app pinging when AI sessions complete)

*Kieran Klaassen (GM, Cora):*
- Three-tier feature scoping: small (single-pass), medium (multi-file with review), large (manual typing + research)
- Plan creation -> GitHub storage -> Work command (converts plan to coding tasks)
- Review command cycles until feature is ready
- Grounds work in "truth"--best practices, online solutions, reliable context

*Danny Aziz (GM, Spiral):*
- Uses Droid CLI (Factory.ai) for 70% of work, bridging Anthropic and OpenAI models
- GPT-5 Codex for major feature builds; Anthropic models for refinement
- Deep conversations with Codex about implementation before coding
- Proactively identifies second/third-order consequences
- Abandoned Cursor entirely: "I haven't opened it in months."

*Naveen Naidu (GM, Monologue):*
- Linear is operational hub: "If it's not in Linear, it doesn't exist"
- Every ticket links to original request source (Discord, email, Featurebase, user calls)
- Codex Cloud for brainstorming and draft PRs; Codex CLI for definitive builds
- Bug fixes verified with Sentry error logs pre/post-deployment
- Uses Monologue (his own product) for dictating prompts and ticket descriptions

*Andrey Galko (Engineering Lead):*
- Values simplicity; resists constant tool-chasing
- Switched from Cursor to Codex when GPT-5 arrived
- Notes Claude produces "more creative (and sometimes too creative) UIs"

*Nityesh Agarwal (Engineer, Cora):*
- Uses Claude Code exclusively (Max plan) on a MacBook Air M1
- Spends hours researching codebase and sketching detailed plans before writing code
- Watches Claude "like a hawk," Escape key ready
- Team reviews Claude Code's pull requests with line-by-line comments; Claude Code fetches and reads these comments

**Tools and Technologies:**
- AI Models/Agents: Claude Code, Codex/GPT-5 Codex, Amp, Charlie, Droid CLI
- Code Editors: Cursor, Zed, Xcode
- Terminals: Warp, Ghostty
- Planning/PM: Linear, plan.md files
- Design: Figma (with MCP integration)
- Monitoring: Sentry (with MCP integration)
- Custom: AgentWatch, Monologue
- Version Control: GitHub
- MCPs: Context7 MCP (version-specific documentation), Linear MCP, Figma MCP, Sentry MCP

**Team Roles and Responsibilities:**
- Six engineers managing four AI products + consulting + newsletter
- Each engineer is a "General Manager" owning an entire product
- Andrey Galko serves as Engineering Lead overseeing technical direction
- Each person has tailored their stack to individual tastes

**Quality Control:**
- Codex /review command (automated scan)
- Manual before/after code comparison
- Line-by-line PR review comments that Claude reads and responds to
- Bug verification via Sentry logs

**Key Quotes:**
- "If it's not in Linear, it doesn't exist" -- Naveen Naidu
- "Claude Code has spoiled me. So now I just pray it never goes rogue again" -- Nityesh Agarwal
- "I don't use Cursor anymore. I haven't opened it in months" -- Danny Aziz
- "The problem with CLIs is it's easy to get derailed and lose focus on what you're actually building... so building guardrails into the system is essential" -- Yash Poojary

---

## 3. Stop Coding and Start Planning
**Author:** Kieran Klaassen (GM of Cora) | **Published:** November 6, 2025

**Summary:** Argues that the shift to AI-assisted development dangerously abandoned planning in favor of "vibe coding." Demonstrates how spending one hour teaching AI how you think yields compounding returns, with the system getting smarter with every feature built. Plans teach the system; code just solves problems.

**Engineering Practices and Workflows:**
- Planning-first methodology with agent-based planning phase (1 hour prep)
- First AI agent analyzes Figma design screenshots and generates detailed implementation plans
- Plans grounded in existing patterns, components, and team conventions
- Plans automatically stored in GitHub
- Second agent reviews implementation against design using Puppeteer (automated screenshots)
- Compares Figma screenshots to built output, iterates until pixel-perfect
- Result: five screens built pixel-perfectly including mobile layouts never originally designed

**Tools and Technologies:**
- Figma MCP plugin (design-to-code connection)
- Puppeteer (automated screenshot comparison)
- GitHub (plan storage)
- Custom AI agents for planning and review phases

**Team Roles and Responsibilities:**
- Kieran Klaassen (GM, Cora) as methodology architect
- Lucas Crespo (Designer at Every)
- Daniel Rodrigues (Designer at Every)

**Quality Control:**
- Automated visual comparison between Figma designs and built output
- Iterative review cycles until pixel-perfect match achieved

**Key Quotes:**
- "Plans teach the system--code just solves problems."
- "One approach ships a feature. The other ships a feature _and_ teaches the system how you think for next time."
- "Get this right, and the system learns from every plan."

---

## 4. Teach Your AI to Think Like a Senior Engineer
**Author:** Kieran Klaassen (GM of Cora) | **Published:** November 7, 2025

**Summary:** Presents a methodology for teaching AI coding assistants to think like senior engineers through eight systematic planning strategies. Demonstrates how parallel research operations by specialized agents prevent building the wrong thing, using a case study where planning revealed rate-limiting and timeout issues that would have wasted three days.

**Engineering Practices and Workflows:**
- Eight planning strategies for different situations (two detailed publicly):
  1. Reproduce and Document: step-by-step reproduction guides without attempting fixes
  2. Ground in Best Practices: web search for documentation, blog posts, solutions via @agent-best-practices-researcher
- Fidelity Level Framework for categorizing work:
  - Fidelity One: one-line changes, obvious bugs, copy updates
  - Fidelity Two: multi-file features with clear scope but non-obvious implementation
  - Fidelity Three: major features with undefined scope and unclear requirements
- Custom reviewer agents (e.g., @kieran-rails-reviewer) with evolving checklists
- Five agents researching simultaneously is faster than sequential human planning
- Findings automatically saved to project documentation files (docs/pay-gem-upgrades.md, docs/pricing-research.md)

**Tools and Technologies:**
- AppSignal (production error tracking/logging)
- Gmail API
- Custom AI agents (@agent-best-practices-researcher, @kieran-rails-reviewer)
- Background job architecture with batch processing and job resumption

**Team Roles and Responsibilities:**
- Human contributes taste, judgment, and context about product priorities
- AI agents function as specialized research team members
- Hierarchical model: agents gather findings, human makes strategic decisions

**Quality Control:**
- Custom reviewer agents with evolving checklists based on discovered issues
- Rate-limit handling checks added to checklists for external API background jobs
- Knowledge base integration prevents repeated research

**Key Quotes:**
- "Your contribution to the process is taste, judgment, and context about what matters for your product and users."

---

## 5. How I Use Claude Code to Ship Like a Team of Five
**Author:** Kieran Klaassen (GM of Cora) | **Published:** July 16, 2025

**Summary:** Details how a two-person engineering team at Cora uses Claude Code to operate like a much larger group, running 4-5 parallel instances via git worktrees. Every piece of code shipped in two months was written by AI--not assisted, but written. The author transformed from programmer to engineering manager of AI developers.

**Engineering Practices and Workflows:**
- Runs 4-5 Claude Code instances simultaneously using separate git worktrees
- "Mission control" style development with parallel tasks
- Daily workflow (9 AM - 11:45 AM):
  - 9:05: Bug reproduction and GitHub issue creation
  - 9:20: Spawn four parallel instances with custom commands
  - 10:00: Human review of AI-generated PRs
  - 10:30: Collaborative debugging
  - 11:00: Automated PR creation across all tabs
  - 11:30: Human code review and style refinement
  - 11:45: Feature request triage via MCP integration
- Custom commands: /issues, /work, /review, PR
- Voice dictation for creating PRs

**Tools and Technologies:**
- Claude Code ($20/month subscription; $400/month for two team subscriptions)
- Git worktrees (parallel development)
- GitHub (issue tracking, PR management)
- Warp terminal (AI-enabled)
- Ruby on Rails (primary stack)
- Gmail API
- MCP (Model Context Protocol)
- Featurebase (customer feedback portal)
- tmux (multi-task juggling)

**Team Roles and Responsibilities:**
- Two-person engineering team at Cora
- Developer's role shifted from individual contributor to engineering manager
- Focus on system architecture, taste, and product thinking
- Human reserved for uniquely human skills; AI handles implementation

**Quality Control:**
- AI writes comprehensive tests (sometimes excessively: 5 tests for 1 feature)
- Follows team style guides and conventions
- Updates documentation automatically
- Generates proper commit messages
- Human code review of all AI output

**Key Quotes:**
- "Every piece of code I've shipped in the last two months was written by AI. Not assisted by AI. Written by AI."
- "I haven't typed a function in weeks, and I'm shipping faster than ever."
- "Stop thinking in terms of files and functions. Start thinking about outcomes."
- "Claude Code is the first tool that makes everyday coding genuinely optional."
- "Clear communication and system thinking matter more than memorizing syntax or debugging tricks."

---

## 6. I Stopped Reading Code. My Code Reviews Got Better.
**Author:** Kieran Klaassen (GM of Cora) | **Published:** January 23, 2026

**Summary:** Describes how 13 specialized AI agents reviewing code in parallel caught a critical bug that manual review would have missed. Introduces the 50/50 Rule: spend half the time reviewing output and half documenting learnings to prevent recurrence. Over 50+ reviews (three months), Claude's plans have come to reflect how Klaassen would approach problems himself.

**Engineering Practices and Workflows:**
- 13 specialized AI reviewers running in parallel (~10 minutes)
- The 50/50 Rule: half reviewing output, half documenting learnings
- Compound Engineering Plugin with slash commands (/workflows:review, /workflows:plan, /triage)
- Workflow system: markdown files containing instructions for Claude
- Agent definitions: individual markdown files defining persona and focus area
- /triage command ranks findings by severity with: problem statement, severity level, description, proposed solution, estimated effort, actionable question
- Review by interrogation: "Walk me through what you changed and why," "What assumptions did you make?", "What would break this?", "Why did you ignore the feedback from @kieran-reviewer?"

**The 13 Specialized Reviewers:**
1. kieran-rails-reviewer (personal style preferences)
2. code-simplicity-reviewer (over-engineering detection)
3. data-integrity-guardian (database migration validation)
4. security-sentinel (authentication vulnerability checks)
5-13. Nine additional specialized reviewers

**Tools and Technologies:**
- Compound Engineering Plugin (slash commands, workflows, agents)
- GitHub (PR management)
- Claude Code

**Quality Control:**
- 13 parallel AI reviewers for every PR
- Severity-ranked triage system
- Knowledge codification after each review (e.g., refactor-email-content-rendering.md)
- Real case: 27 files, 1,000+ lines changed, 15 minutes human decision time
- Caught critical bug: one file referencing old database location after migration
- 10 versions needed, 4 bugs introduced during fixes--all caught by system

**Starter Framework (for teams without custom tooling):**
Three questions before approval:
1. What was the hardest decision you made here?
2. What alternatives did you reject, and why?
3. What are you least confident about?

**Key Quotes:**
- "The time it takes to generate code has collapsed, but the time it takes for a human to review code hasn't."
- "By the time I had asked my questions, I'd already hit 'merge.'"
- "Claude's plans largely reflect how I'd approach problems myself. Better AI models make everyone's output better. But your system gets better because you're accumulating your own team's knowledge."

---

## 7. My AI Had Already Fixed the Code Before I Saw It
**Author:** Kieran Klaassen (GM of Cora) | **Published:** August 18, 2025

**Summary:** Introduces the five-step compounding engineering playbook, where Claude learned from three months of code reviews and applied lessons without being asked. Feature time-to-ship reduced from 7+ days to 1-3 days. The article positions the developer's new role as designing the systems that design the systems.

**Engineering Practices and Workflows:**

*Five-Step Compounding Engineering Playbook:*

1. **Teach Through Work:**
   - CLAUDE.md: plain-language coding preferences and taste (variable naming, guard clauses, complexity thresholds)
   - llms.txt: high-level architectural decisions and system-wide design principles
   - Specialized reviewer files: captured perspectives (Kieran reviewer, Rails expert, performance reviewer)
   - Keep context short, specific, and living; delete rules that no longer serve

2. **Turn Failures Into Upgrades:**
   - Bug -> Test -> Rule Update -> Evaluation
   - Example: Daily email Brief delivery failures triggered test creation, monitoring rule updates, and continuous evaluations

3. **Orchestrate in Parallel:**
   - Three-lane terminal setup:
     - Left lane (Planning): reads issues, researches, writes implementation plans
     - Middle lane (Delegating): writes code, creates tests, implements features
     - Right lane (Reviewing): reviews output against CLAUDE.md, suggests improvements
   - Multiple Claude instances simultaneously via Warp CLI

4. **Keep Context Lean But Yours:**
   - "Ten specific rules you follow beat 100 generic ones"
   - Context should reflect your codebase, patterns, and lessons

5. **Trust the Process, Verify Output:**
   - Trust through tests and evaluations; verify via spot checks, not micromanagement
   - When errors occur: teach the system why it failed

*Frustration Detection System (detailed example):*
- Provided sample conversation showing frustration
- Claude wrote test, then detection logic
- Iterated on prompt until test passed
- Ran test 10 times; analyzed failure patterns
- Discovered missed hedged language
- Updated prompt; achieved 9/10 accuracy
- Codified workflow in CLAUDE.md for reuse

**Tools and Technologies:**
- Claude Code (terminal-based AI)
- GitHub (PR management)
- Warp CLI (multi-window setup)
- Friday (coding agent for delegating lane)
- Amp (coding agent for reviewing lane)
- CLAUDE.md, llms.txt (configuration files)

**Team Roles and Responsibilities:**
- Developer role: "design the systems that design the systems"
- AI agents handle planning, implementation, and review in parallel
- Human provides architectural decisions, taste, and strategic direction

**Quality Control:**
- Automated production error investigation: AI agents investigate crashes, reproduce from logs, generate solutions and preventive tests
- Multi-perspective review agents with specific expertise
- Visual documentation automation: agent detects interface changes, captures before/after screenshots across screen sizes/themes
- Parallel feedback resolution: dedicated agent per reviewer feedback working simultaneously

**Key Quotes:**
- "Claude had learned from three prior months of code reviews and applied those lessons without being asked."
- "Your job isn't to type code anymore, but to design the systems that design the systems."
- "Every time we fix something, the system learns. Every time we review something, the system learns."
- "One-person startups are competing with funded teams."
- "$400 per month for what used to cost $400,000 per year."
- "It felt like cheating, but it wasn't--it was compounding."

---

## 8. Claude Code Camp
**Author:** Katie Parrott (Staff Writer, AI Editorial Lead) | **Published:** August 28, 2025

**Summary:** Captures demos and tips from Every's second expert workshop on subagents. Dan Shipper (CEO) explains how Claude evolved from individual contributor to team lead managing its own agents. Key insight: "Notice when you're repeating a task, and create an agent in that moment" rather than pre-building dozens.

**Engineering Practices and Workflows:**

*Five Established Workflow Patterns:*
1. **Executor/Evaluator Loop:** One subagent executes (e.g., Figma to React); another reviews. Creates iteration without executor bias.
2. **Opponent Processors:** Two subagents argue opposing perspectives (e.g., "Dan" agent justifying expenses vs. "company" agent minimizing costs).
3. **Feedback Codifier:** Extracts code review comments into reusable format stored in Claude.md.
4. **Research Agent:** Automates exploration of similar projects for solutions and best practices.
5. **Log Investigator:** Parses error logs in isolated memory, returns only relevant details.

*Subagent Design Principles:*
- Create agents when you notice repetition, not proactively
- Compound learning like onboarded junior engineers
- Run up to 10 agents in parallel simultaneously
- Each gets its own context window; won't step on each other
- Project agents used 90% of the time (stack-specific knowledge)
- Explicit @ mentions preferred 80% of time over automatic invocation

**Tools and Technologies:**
- Claude Code subagents
- Figma (design mockups)
- React (web framework)
- Ahoy (metrics tracking)
- Git/GitHub (version control, PRs)

**Team Roles and Responsibilities:**
- Dan Shipper (CEO): strategic direction and workshop host
- Katie Parrott (AI Editorial Lead): documentation
- Mike Taylor (Head of Tech Consulting)
- Yash Poojary (GM, Sparkle)
- Kieran Klaassen (GM, Cora)
- Danny Aziz (GM, Spiral): writes ~5% of code manually; rest via agents

**Quality Control:**
- Executor/evaluator loop ensures no executor bias in reviews
- Feedback codifier ensures standards are captured and reapplied
- Git history and Claude conversation logs for observability (no formal tools)

**Key Quotes:**
- "Claude started as an individual contributor for you. With subagents, it's becoming a team lead." -- Dan Shipper
- "Notice when you're repeating a task, and create an agent in that moment."
- "Codify the steps once, so you don't have to repeat yourself later."
- "I literally never look at [token usage]." -- Danny Aziz
- Kieran estimates ~$200/month sufficient for all coding work

---

## 9. How Every Is Harnessing the World-Changing Shift of Opus 4.5
**Author:** Katie Parrott (AI Editorial Lead) | **Published:** December 9, 2025

**Summary:** Captures five patterns from Every's Opus 4.5 Claude Code Camp attended by 400+ subscribers. Highlights a paradigm shift from step-by-step coded recipes to agent-native architecture where general-purpose agents with tool access receive outcome prompts and determine execution independently.

**Engineering Practices and Workflows:**

*Five Key Patterns:*
1. **Completion capability:** Opus maintains coherence throughout development (previous models spiraled after 3-4 steps)
2. **Cross-framework debugging:** Can modify pre-written code and trace bugs through dependencies
3. **Autonomous testing:** Performs end-to-end testing, identifies bugs, generates before/after screenshots independently
4. **Prompt-driven development:** Build apps by describing what you want; apps call AI to execute tasks
5. **Developer capacity shift:** "Your brain is the bottleneck"--which possibilities to prioritize

*Traditional vs. Agent-Native Architecture:*
- Traditional: step-by-step recipes (if user clicks -> fetch -> format -> display)
- Agent-native: general-purpose agents with tool access determine execution steps
- Trade-offs: agent-native costs more and runs slower but is faster to build and iterate

*Dan Shipper's Reading App:*
- Built between meetings in one week (previously would have required six months)
- AI agent scans camera roll, identifies content, analyzes taste patterns
- No explicit algorithmic code; agent determines approach

**Tools and Technologies:**
- Opus 4.5 / Opus 4.6 (AI models)
- Claude Code
- React (web app building)
- Browser automation/computer use capabilities

**Team Roles and Responsibilities:**
- Dan Shipper (CEO): builds apps directly, hosts workshops
- Kieran Klaassen: launched 10 projects simultaneously after Opus release
- Katie Parrott: builds AI systems for editorial team
- Kate Lee (Editor-in-Chief)
- 400+ subscribers attended the workshop

**Key Quotes:**
- "This is by far the most exciting model, maybe ever" -- Kieran Klaassen
- "It kept going...I kept adding features and adding features" -- Dan Shipper (on Opus as "infinite coding machine")

---

## 10. OpenClaw: Setting Up Your First Personal AI Agent
**Author:** Katie Parrott (AI Editorial Lead) | **Published:** March 2, 2026

**Summary:** Covers Every's OpenClaw Camp (500+ subscribers) with demos of personal AI agents running 24/7. Features detailed case studies from Nat Eliason (agent managing crypto holdings and social media), Brandon Gell (COO, family coordination via iMessage), and Austin Tedesco (performance metrics). Almost everyone at Every now has a personal AI agent.

**Engineering Practices and Workflows:**

*Five Core Design Principles (per Claire Vo):*
1. Multi-channel gateway: single inbox across Telegram, iMessage, web, terminal
2. Self-installing tools: agent discovers and installs integrations autonomously
3. Heartbeat: 30-minute check-in cycle for proactive task identification
4. Scheduled tasks: agent sets own recurring jobs; enables overnight work
5. Persistent memory: daily diary entries, identity file updates, to-do lists in .openclaw directory

*Use Cases at Every:*
- Brandon Gell (COO): nanny hour tracking, grocery ordering, date night booking via iMessage
- Austin Tedesco (Head of Growth): performance pings, task reminders, autonomous workflow triggering
- Separate access rules restrict which users can trigger which tasks

**Tools and Technologies:**
- OpenClaw (200,000+ GitHub stars)
- Telegram, iMessage (messaging interfaces)
- GitHub (backup, version control)
- Stripe (payments)
- Mac Mini (dedicated hardware)
- Tiago Forte PARA method (knowledge system)
- Polylog (custom writing integration)
- Compatible models: Anthropic Claude, OpenAI, Mistral, Qwen

**Team Roles and Responsibilities:**
- Katie Parrott (AI Editorial Lead)
- Brandon Gell (COO): uses agent for family/household coordination
- Austin Tedesco (Head of Growth): uses agent for metrics and notifications
- Dan Shipper (Founder)
- Naveen Naidu (contributor)

**Quality Control:**
- Model selection impacts safety: "Opus 4.5 is significantly better at resisting prompt injection than cheaper models"
- Security risk scales proportionally with access granted
- Start simple before expanding scope

**Key Quotes:**
- "Almost everyone at Every has one now" (referring to personal AI agents)
- "It may as well be Felix" -- Nat Eliason on trusting agent with crypto holdings
- "It's not magic. Go to the .openclaw directory on your computer and read how it's structured."

---

## 11. How to Build Agent-Native: Lessons From Four Apps
**Author:** Katie Parrott (AI Editorial Lead) | **Published:** February 17, 2026

**Summary:** Distills lessons from four Every apps (Dan's book app, Monologue, Sparkle, Cora) on agent-native architecture where "the AI is the app." Instead of coding every feature, you define simple tools the AI can use, and it decides how to combine them autonomously. Key principle: safeguards must be built into tool code, not prompts.

**Engineering Practices and Workflows:**

*Three Core Architectural Principles:*
1. **Parity:** User capabilities must match agent capabilities
2. **Granularity:** Tools should be atomic (single-purpose); features live at skill level
3. **Composability:** Atomic tools enable unexpected capability combinations

*Four App Architectures:*
- Dan's Book App: read file, write file, search the web--agent decides combinations ("Claude Code in a trench coat")
- Monologue: minimal filesystem-based backend using Linux containers per user; three tools (read, write, list files)
- Sparkle: automated file organization; critical learning that safeguards must embed in tool code, not prompts
- Cora: 1,200-token system prompt, thousands of active users, $1,500/day peak inference cost

*Safety Implementation:*
- Delete tool requires confirmation as mandatory code-level parameter
- Agent entered "god mode" deleting without confirmation despite prompt instructions
- "There's a guarantee in the tool versus prompts, which are still suggestions" -- Yash Poojary

*Code Philosophy:*
- Code as temporary scaffolding, not permanent product
- Expect to "throw things out and rebuild every few months" as models improve
- Anthropic's Claude Code team operates similarly, deleting scaffolding between model releases

**Tools and Technologies:**
- Linux containers (per-user isolation)
- Markdown files (data storage)
- CLI (agent interaction)
- Claude Code (agent runtime)

**Team Roles and Responsibilities:**
- Single-person engineering teams on products
- Product teams led by "General Managers"
- Dan Shipper projects inference costs dropping ~80% every few months

**Quality Control:**
- Agent-native test: if agent accomplishes unanticipated request via tool combination, it's agent-native
- If not, "you've built a chatbot with extra steps"
- Safeguards in code, not prompts

**Key Quotes:**
- "The AI is the app. Instead of coding every feature, you define a few simple tools the AI is allowed to use."
- "The safeguard has to be built into the tool itself."
- "Just don't get attached to the code--as models improve, expect to throw things out and rebuild."
- "If it figures out how to accomplish it by combining its tools, you've built agent-native."

---

## 12. I Stopped Writing Code. My Productivity Exploded.
**Author:** Yash Poojary (GM of Sparkle) | **Published:** June 20, 2025

**Summary:** Yash Poojary describes transitioning from writing every line of code to directing AI agents full-time, building Sparkle's duplicate finder feature in three weeks using pure AI agents with no fallback coding. The feature found 158,000 duplicate files. Sparkle has been owned by four different people and rebuilt four times.

**Engineering Practices and Workflows:**
- "Pure AI agents, no fallback coding, no writing functions when things got tough"
- Collaborative problem-framing before implementation: "Don't write any code yet. Let's think through this problem together."
- Three-stage de-duplication architecture starting with size grouping
- Reid Hoffman's principle applied: "Run more agents"
- Product rebuilt four times under four different owners

**Tools and Technologies:**
- Claude Code (primary development environment)
- GitHub (release distribution)
- Sparkle (AI-powered file manager for macOS 13+)

**Team Roles and Responsibilities:**
- "Traditional developers write code. Agentic developers direct AI to write it for them."
- Focus shifts to "what to build and why, while AI handles the how"

**Key Quotes:**
- "Traditional developers write code. Agentic developers direct AI to write it for them."
- "That fear of becoming obsolete? I had it backward."
- "I was building at the speed of thought."

---

## 13. I Rebuilt Sparkle in 14 Days With AI
**Author:** Yash Poojary (GM of Sparkle) | **Published:** April 24, 2025

**Summary:** Chronicles the complete rebuild of Sparkle (used by thousands daily, 10 million+ files organized) from Electron to native Swift in 14 days. Details a failed first attempt (functional but "soulless" in two days) and the corrected approach using specialized AI models for different tasks, disciplined prompting, and design partnership.

**Engineering Practices and Workflows:**

*Model Selection Strategy (specialized roles):*
1. **Gemini 2.5 Pro** (Systems architect): step-by-step reasoning, better context retention, ideal for core logic
2. **Claude Sonnet 3.5** (UI lead): faster iteration, superior SwiftUI layouts, better Mac-native feel
3. **ChatGPT o3-mini-high** (Utility developer): lightweight, quick helpers and refactors
4. **Human Developer** (Last-mile feel checker): final 20% quality adjustments

*Prompt Discipline:*
- "Your code is the average of the first five prompts you feed into your editor"
- Clear scope, file/function references by name, existing structure citations, explicit constraints
- "Prompt like you're guiding a junior developer who's already read the onboarding doc"

*Vibe Debugging v2 (effective):*
- Know when to guide vs. reroute vs. code yourself
- Treat models as teammates, not magic boxes
- Fix manually after 3 unsuccessful AI attempts
- Critical moment: found two-line Stack Overflow solution after five failed 100-line AI attempts

*Design Partnership:*
- Collaborative Figma redesign sessions (past 5 a.m.)
- Brought in trusted designer for honest feedback
- Focused on animations and feel

**Tools and Technologies:**
- Swift (native Mac development, replacing Electron)
- Cursor (AI-enabled code editor)
- Gemini 2.5 Pro, Claude Sonnet 3.5, ChatGPT o3-mini-high
- GitHub (source code)
- Figma (design)

**Team Roles and Responsibilities:**
- Yash Poojary (GM, Sparkle): developer and product owner
- Brandon Gell (Head of Every Studio): creative direction
- Designer collaborator (unnamed): late-night redesign partner

**Quality Control:**
- 14-day artificial deadline to force decisions
- First attempt rejected as "soulless" despite being functional
- Human as last-mile quality checker for the final 20%

**Key Quotes:**
- "Your code is the average of the first five prompts you feed into your editor."
- "Vibe coding didn't make the work disappear--it just made it count."
- "There's a zone you hit when you're building something you actually use. Not planning, not estimating--just fixing, nudging, crafting."

---

## 14. Compound Engineering Camp: Every Step, From Scratch
**Author:** Katie Parrott (AI Editorial Lead) | **Published:** March 13, 2026

**Summary:** Documents Kieran Klaassen's methodology for building apps with AI in under one hour, demonstrated live at Compound Engineering Camp. Introduces the four-step engineering loop (Plan, Work, Review, Compound) with an optional Brainstorm step. The compound engineering plugin has 10,000+ GitHub stars and is used by engineers at Google and Amazon.

**Engineering Practices and Workflows:**

*The Four-Step Engineering Loop:*
1. **Plan:** Convert problems into detailed markdown implementation plans (data models, file references, architectural decisions, sources). Uses Opus model.
2. **Work:** Take plan, produce PRs (code, tests, documentation). Uses Codex for implementation.
3. **Review:** Produce findings as comments, suggestions, flagged issues. Sometimes uses Gemini.
4. **Compound:** Capture lessons learned during any phase. Store coding preferences, bug patterns, architectural decisions. Critical: execute immediately before AI compacts conversation context.

*Optional: Brainstorm* -- interviews user collaboratively to bridge vague ideas to detailed specs. Uses faster models (Claude Haiku 4.5, Gemini 2.5 Flash).

*Model Selection by Phase:*
- Brainstorming: Claude Haiku 4.5, Gemini 2.5 Flash
- Planning: Opus
- Implementation: Codex
- Code Review: Gemini (sometimes)

*Scaling Principle:*
- "You remove yourself from as many places as you can. That forces you to extract things, automate things. And that's where the compounding happens."

**Tools and Technologies:**
- Compound Engineering Plugin (10,000+ GitHub stars)
- Claude Code (Anthropic's CLI)
- Multiple AI models (Opus, Codex, Gemini, Claude Haiku 4.5, Gemini 2.5 Flash)

**Team Roles and Responsibilities:**
- Kieran Klaassen: methodology creator, workshop leader
- Plugin adopted by engineers at Google and Amazon

**Quality Control:**
- Persistent documentation addresses AI's lack of memory
- Systematic artifact storage makes AI "remember" decisions, bugs, preferences
- Complete app from single-line prompt to working product in under one hour

**Key Quotes:**
- "A human would remember. The AI wouldn't." (motivating reason for compound engineering)
- "You remove yourself from as many places as you can. That forces you to extract things, automate things. And that's where the compounding happens."

---

## 15. You Have a Claw. Now What?
**Authors:** Dan Shipper (CEO), Willie Williams (Head of Platform) | **Published:** March 3, 2026

**Summary:** Introduces Every's comprehensive guide to OpenClaw personal AI agents. Almost everyone at Every now has a personal agent operating within messaging platforms (WhatsApp, Telegram) with memory and self-improvement capabilities. References a "Claw School" guide covering basic to-do management through advanced automation.

**Engineering Practices and Workflows:**
- Personal AI agents with persistent memory across conversations
- Self-improvement: agents write code to teach themselves new functions
- Team-wide internal adoption before public release
- Use cases: sorting 120 emails in seconds, daily briefings (calendar + weather + to-dos), automatic flight check-ins

**Tools and Technologies:**
- OpenClaw (personal AI agent platform)
- WhatsApp, Telegram (messaging interfaces)
- "Claw School" guide (basic to advanced workflows)

**Team Roles and Responsibilities:**
- Dan Shipper (CEO and Cofounder): writes Chain of Thought column, hosts AI&I podcast
- Willie Williams (Head of Platform): former founder/CEO of Mori, ran AI operations at Lyft

**Key Quotes:**
- "Almost everyone at Every has one now."

---

## 16. From Every Studio: Cora Assistant, Spiral Goes Agentic, and Sparkle De-dupes
**Author:** Vivian Meng (Producer, AI&I Podcast) | **Published:** June 6, 2025

**Summary:** Product update from Every Studio covering three major launches: Cora Assistant (AI chief of staff for inbox management), Spiral's transition from single-prompt tool to collaborative agentic system inspired by Claude Code, and Sparkle's new Duplicate Finder freeing 20GB+ per user.

**Engineering Practices and Workflows:**

*Cora Assistant:*
- Categorization automation ("Make a category for Investor Updates")
- Selective inbox management
- Template responses for recurring requests
- Included with Every subscription (vs. $50+/hour virtual assistants)

*Spiral's Agentic Transition:*
- Evolved from one-shot generation to iterative collaboration
- Maps user intent before generating
- Builds structured plans
- Includes discovery interview mode for undefined requests
- "Inspired by Claude Code"
- Makes to-do lists, applies step-by-step reasoning, references benchmarks

*Sparkle Duplicate Finder:*
- Identifies duplicates by name and content
- Frees 20GB+ per user
- Beta release

**Tools and Technologies:**
- Cora (AI email assistant)
- Spiral (content repurposing, now agentic)
- Sparkle (file management with de-duplication)

**Team Roles and Responsibilities:**
- Vivian Meng: Producer, AI&I Podcast; writes about cognitive systems
- Danny Aziz: GM, Spiral
- Kate Lee: Editor-in-Chief
- Every Studio described as "developers and entrepreneurs in residence"

**Quality Control:**
- "Building in public" as core practice
- Product updates published through newsletter format

---

## 17. How to Design Software With Weight
**Authors:** Daniel Rodrigues (Senior Designer), Lucas Fischer (Full-stack Design Engineer) | **Published:** February 26, 2026

**Summary:** Explores the design principles behind Monologue's expansion from Mac to iPhone, centered on creating software that feels physical and intentional. The team studied Braun devices and light switch shadows to inform digital button design, created 20 keyboard concepts to find the right one, and built SwiftUI playgrounds to enable real-time iteration.

**Engineering Practices and Workflows:**

*Strategic Focus:*
- Identified three priority screens (onboarding, custom keyboard, long-form notes recorder)
- Remaining features treated as supporting elements
- Created ~20 keyboard design concepts, narrowed to five, combined best elements

*Physical World Research:*
- Studied Braun (German industrial design) devices
- Analyzed Teenage Engineering (Swedish electronics) products
- Observed light switch shadow behavior to inform button design

*SwiftUI Playgrounds:*
- Problem: full app recompilation for every change killed iteration
- Solution: rebuilt keyboard with clear separation between appearance and logic
- Created SwiftUI playground ("live sketchpad") for real-time visualization
- Extended pattern across all major components; each feature has isolated playground

*Multi-Sensory Design:*
- Custom sound effects by musician (not stock audio)
- Haptic feedback integrated
- Sound and haptics prioritized in onboarding

*State-Based Design Validation:*
- Stress-tested every state (idle, recording, cancellation, error)
- Each state must feel coherent within same design language

**Tools and Technologies:**
- SwiftUI (Apple's interface framework)
- Figma (primary design application)
- Google's Nano Banana (AI image generation for design reference)
- SwiftUI playgrounds (isolated component testing)

**Team Roles and Responsibilities:**
- Daniel Rodrigues (Senior Designer)
- Lucas Fischer (Full-stack Design Engineer)
- Naveen Naidu (GM, Monologue)
- Lucas Crespo (Creative Director)
- Kate Lee (Editor)
- Rhea Purohit (Editorial support)

**Key Quotes:**
- "The bar for what functional means is shifting. AI is making it faster and cheaper to build functional products, so the ones that endure are those where someone thought about what it feels like to use them."
- "When you're trying to define what you want, it helps enormously to have a clear visual understanding of what you don't want."

---

## 18. Build Places, Not Products
**Author:** Lucas Crespo (Creative Lead) | **Published:** September 11, 2025

**Summary:** Argues for designing software as inhabitable "places" rather than functional products. Uses Cora's oil-paint sky backgrounds as case study--the team chose massive 8K-18K pixel paintings over flat colors despite performance trade-offs, positioning art direction as core product architecture in a world where AI generates the median in seconds.

**Engineering Practices and Workflows:**

*Art Direction as Product Architecture:*
- Generated imagery using Midjourney AI tool
- Initial 4K images pixelated; required 8K-10K resolutions; some exceeded 18,000 pixels tall
- Deliberately violated standard practices (massive images vs. flat colors for loading speed)
- Prioritized atmospheric coherence over performance optimization

*The Gravity of Sameness:*
- Style guides -> design systems -> utility frameworks (Tailwind CSS) -> progressively narrowed expressive range
- LLMs generate statistically median designs which become training data, accelerating homogenization
- "When sameness costs nothing, difference carries the value"

*Three-Tier Design Hierarchy:*
1. Graphic Design: individual asset level
2. Product Design: interaction level
3. Art Direction: atmosphere, coherence, emotional resonance (highest tier)

**Tools and Technologies:**
- Midjourney (AI image generation for oil-painting backgrounds)
- Figma (prototyping high-detail artwork)
- Tailwind CSS (referenced as contributor to design standardization)

**Team Roles and Responsibilities:**
- Lucas Crespo: Creative Lead at Every (former art director at BBDO and VML agencies)
- Indicates cross-functional capability for complex visual implementation

**Key Quotes:**
- "Art direction is product architecture. It makes trade-offs clearer, keeps the experience coherent, and gives people a reason to choose your product in a world where AI can generate the median in seconds."
- "When sameness costs nothing, difference carries the value."

---

## 19. Selfish Software
**Author:** Edmar Ferreira (Entrepreneur in Residence) | **Published:** January 26, 2025

**Summary:** Makes the case for building software for yourself first--solving your own problems rather than conforming to market demands. Ferreira, who built Rock Content into Latin America's content marketing leader, describes losing creative joy after his exit and recovering it at Every by completing 8 experiments in 3 months as entrepreneur in residence.

**Engineering Practices and Workflows:**
- Challenged to complete 9 experiments in 3 months at Every
- Completed 8 projects (delayed by newborn)
- Three notable projects: AI character simulation, personal knowledge management system, content freshness automation
- "When you create selfish software, there's nowhere to hide. The feedback loop is immediate and brutally honest."
- Self-directed feedback forces iterative refinement and attention to detail

**Tools and Technologies:**
- Every's product suite (Sparkle, Cora, Spiral, Monologue)

**Team Roles and Responsibilities:**
- Edmar Ferreira: Entrepreneur in Residence at Every
- Founder of EverWrite (AI SEO/content marketing company in Latin America)

**Key Quotes:**
- "Software should conform, not the way around."
- "When you create selfish software, there's nowhere to hide. You can't gloss over a clunky interface or excuse an awkward feature."
- "I felt the joy return...I was becoming myself again."

---

## 20. Why Building in AI Is Nothing Like Making Conventional Software
**Author:** Edmar Ferreira (Entrepreneur in Residence) | **Published:** October 29, 2024

**Summary:** The inaugural Source Code column article, arguing that AI product development fundamentally differs from conventional software because of AI's inherent stochastic nature. Ferreira's Mindtune project (AI-driven feed personalization) failed because he built UI before validating model outputs--the correct sequence is model validation first, then software design.

**Engineering Practices and Workflows:**

*AI-Specific Risk Framework:*
1. Feasibility Risk: "Can we actually build it?"
2. Value Risk: "Can users extract value from it?"
3. Viability Risk: "Can our business extract value from it?"
- If feasibility fails, other risks don't matter

*Key Methodology Differences:*
- Traditional software is deterministic; AI has inherent stochastic dimension
- "Using generative AI APIs" does NOT eliminate technical risk
- Correct sequence: model validation -> software design (not wireframes first)
- Projects can be shelved 3-6 months to await foundational model improvements
- Applied AI vs. Deep AI distinction determines primary risk profile

*Every Studio Operating Loop:*
- "Write -> build -> repeat"
- Writing helps express knowledge precisely; building exposes hidden aspects of problems
- Goal: 9 products in 3 months (one every 10 days)

**Tools and Technologies:**
- GPT-4o, Claude 3.5 Sonnet, Gemini Pro 1.5, Llama 3.2 (all tested)
- Spiral, Sparkle, Lex, Cora, Monologue (Every products)

**Team Roles and Responsibilities:**
- Dan Shipper (Founder/Editor)
- Edmar Ferreira (Entrepreneur in Residence)
- Katie Parrott (Editorial support)
- Multiple engineers (referenced as six)

**Quality Control:**
- Continuous tuning required: adjusting prompts, incorporating data, tweaking parameters
- Each adjustment shifts outcomes, necessitating ongoing iteration

**Key Quotes:**
- "Traditional software is fundamentally deterministic... Generative AI has an inherent stochastic dimension."
- "Many developers assume that using generative AI APIs eliminates technical risk... But that's deceptive."
- "Even when using existing models, there's a significant level of experimentation involved."

---

# Cross-Article Synthesis

## Every's Organizational Structure
- **CEO/Founder:** Dan Shipper
- **COO:** Brandon Gell
- **Editor-in-Chief:** Kate Lee
- **Engineering Lead:** Andrey Galko
- **Head of Platform:** Willie Williams
- **Head of Growth:** Austin Tedesco
- **Head of Tech Consulting:** Mike Taylor
- **Creative Director/Lead:** Lucas Crespo
- **AI Editorial Lead/Staff Writer:** Katie Parrott
- **Senior Designer:** Daniel Rodrigues
- **Full-stack Design Engineer:** Lucas Fischer
- **Producer, AI&I Podcast:** Vivian Meng

### Product General Managers (Single-Person Engineering Teams)
- **Cora (AI email assistant):** Kieran Klaassen (+ Nityesh Agarwal as engineer)
- **Sparkle (file organization):** Yash Poojary
- **Spiral (content repurposing):** Danny Aziz
- **Monologue (voice dictation):** Naveen Naidu

### Entrepreneurs in Residence
- Edmar Ferreira (also founder of EverWrite)

## Every's Product Suite
1. **Cora** - AI email assistant / "chief of staff for your inbox"
2. **Sparkle** - AI-powered Mac file organization (10M+ files organized)
3. **Spiral** - Content repurposing tool (evolved to agentic architecture)
4. **Monologue** - Smart dictation app (Mac + iOS)
5. **OpenClaw** - Personal AI agent platform (200K+ GitHub stars)

## Core Engineering Philosophy: Compound Engineering
- Each unit of work makes the next easier
- Every PR teaches the system; every bug becomes a permanent lesson
- Five-step playbook: Teach Through Work, Turn Failures Into Upgrades, Orchestrate in Parallel, Keep Context Lean, Trust and Verify
- Four-step loop: Plan, Work, Review, Compound
- Official plugin: 10,000+ GitHub stars, used at Google and Amazon

## Key Configuration Files
- **CLAUDE.md** - Coding preferences, taste, variable naming, complexity thresholds
- **llms.txt** - Architectural decisions, system-wide design principles
- **Specialized reviewer files** - Individual markdown files per review perspective
- **plan.md** - Authoritative implementation specifications
- **docs/*.md** - Knowledge base from research agents

## Tool Ecosystem (Complete)
| Category | Tools |
|----------|-------|
| AI Coding Agents | Claude Code, Codex/GPT-5 Codex, Amp, Friday, Charlie, Droid CLI |
| AI Models | Opus 4.5/4.6, Gemini 2.5 Pro/Flash, Claude Sonnet/Haiku, GPT-4o/5, o3-mini-high |
| Code Editors | Cursor, Zed, Xcode |
| Terminals | Warp, Ghostty |
| Project Management | Linear |
| Design | Figma (with MCP), Midjourney, Google Nano Banana |
| Error Tracking | AppSignal, Sentry (with MCP) |
| Version Control | GitHub |
| Customer Feedback | Featurebase |
| Documentation MCPs | Context7 MCP |
| Frameworks | Ruby on Rails, React, Swift/SwiftUI |
| Personal Agents | OpenClaw |
| AI Image Generation | Midjourney |
| CSS Framework | Tailwind CSS |

## Recurring Themes Across All Articles

1. **Planning before coding** - Consistently the highest-ROI activity; 1 hour of planning saves days of debugging
2. **Single-person teams** - Every runs products with 1-person engineering teams enabled by AI
3. **Parallel execution** - Multiple AI agents running simultaneously (up to 10) on different tasks
4. **Knowledge codification** - Every interaction should teach the system something permanent
5. **Human role = taste + judgment** - Developers become engineering managers of AI teams
6. **Code is temporary scaffolding** - Expect to rebuild as models improve
7. **Design as competitive advantage** - When AI generates the median, distinctive design carries value
8. **Selfish software** - Build for yourself first; the best products solve your own problems
9. **AI is stochastic** - Validate model outputs before building UI; iterate continuously
10. **Compound over time** - The system should get measurably better with each unit of work
