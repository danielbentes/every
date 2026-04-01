# Workflow: Compound Engineering Feature Cycle

Layer: L2 (Workflow)
Date: 2026-04-01

## Purpose

This workflow produces shipped software features across Every's four products (Spiral, Cora, Monologue, Sparkle) using the compound engineering methodology — a four-step loop where AI agents do 99% of the code writing and the system gets smarter with every cycle. Each feature cycle produces both a working feature and institutional knowledge artifacts (docs/solutions/ entries, CLAUDE.md updates, reusable patterns) that make the next cycle faster.

Why it matters: Every's "Two-Slice Team" model means each product is run by a single GM who is simultaneously the product manager, engineer, designer liaison, and marketer. Compound engineering is what makes this possible — it's not just a development methodology, it's the structural foundation that lets a ~20-person company run four products. The methodology has 12K+ GitHub stars as an open-source plugin and is the core of Every's builder credibility in consulting ("We show what we built").

## Trigger

Any of the following initiates a feature cycle:
1. A GM identifies a feature need through user feedback, metrics, or product strategy
2. A bug is reported that requires more than a trivial fix (trivial fixes follow abbreviated cycle — Work + Review only)
3. Dan Shipper (CEO) or Brandon Gell (CTO) flags a strategic product direction requiring implementation
4. A consulting engagement surfaces a feature need that aligns with product roadmap

## Steps

### Step 1: Plan (40% of total cycle time)
- **Responsible party:** Product GM + AI planning agent
- **Input:** Feature need — could be a user story, a bug report, a strategic objective, or a rough idea
- **Process:**
  1. The GM writes a Product Requirements Document (PRD) that specifies: what the feature does, who it serves, what success looks like, and any constraints.
  2. The AI planning agent researches the existing codebase to understand:
     - Current architecture relevant to the feature
     - Existing patterns in docs/solutions/ that apply
     - CLAUDE.md conventions and constraints
     - Prior attempts at similar features (if any)
  3. The agent produces a detailed plan.md containing:
     - **Objectives:** What specifically will be different when this is done
     - **Architecture:** How the feature fits into the existing system — which files change, which new files are created, which APIs are affected
     - **Step-by-step implementation:** Numbered tasks with dependencies, ordered for execution
     - **Success criteria:** Observable, testable conditions that confirm the feature works
     - **Risk assessment:** What could go wrong, what edge cases exist, what existing flows might break
     - **Relevant prior solutions:** Links to docs/solutions/ entries that inform this implementation
  4. The GM reviews the plan. This is the most critical human judgment moment in the cycle: Is the plan solving the right problem? Is the architecture sound? Are the success criteria actually measuring success?
  5. The GM approves, revises, or rejects the plan. No code is written until the plan is approved.
- **Output:** Approved plan.md committed to the repository
- **Criteria for completion:** GM has reviewed and explicitly approved the plan. Plan contains all six components listed above (objectives, architecture, steps, success criteria, risks, prior solutions).
- **Why 40% of time:** Plans are the primary artifact of compound engineering, not code. A thorough plan means the Work step executes cleanly. A sloppy plan means cycles of revision. "Vibe coding" (jumping to code without a plan) is an explicit anti-pattern.

### Step 2: Work (10% of total cycle time)
- **Responsible party:** AI execution agent (operating in git worktrees)
- **Input:** Approved plan.md
- **Process:**
  1. The agent creates a git worktree for the feature branch (isolating work from the main branch and other in-progress features).
  2. The agent executes the plan step by step, writing code that follows:
     - The architecture specified in the plan
     - Existing codebase conventions documented in CLAUDE.md
     - Patterns from docs/solutions/ referenced in the plan
  3. The agent runs tests as it goes — unit tests, integration tests, linting, type checking.
  4. If the agent encounters a blocker not anticipated by the plan, it documents the deviation and either:
     - Resolves it within the plan's intent and documents the resolution, or
     - Flags it for GM review before proceeding
  5. The agent produces a PR with the complete implementation.
- **Output:** Pull request with all code changes, tests, and a summary of any deviations from the plan
- **Criteria for completion:** PR is created, all tests pass locally, agent's self-assessment confirms plan was followed (or deviations documented)
- **Why 10% of time:** If the plan is thorough, execution is mechanical. The agent translates a well-specified plan into code. This is where AI's speed advantage is most dramatic.
- **GM variation:** Different GMs use different execution approaches — Yash runs parallel Claude+Codex agents, Danny uses the Droid CLI, Naveen works Linear-centric, Kieran is plan-first. The methodology accommodates variation in execution tooling as long as the Plan-Work-Review-Compound structure is followed.

### Step 3: Review (40% of total cycle time)
- **Responsible party:** 14 parallel review agents + Product GM
- **Input:** Pull request from Step 2
- **Process:**
  1. **14 review agents run in parallel.** Each agent evaluates the PR against a specific dimension:
     - Security vulnerabilities
     - Performance impact and regressions
     - Architecture alignment with existing patterns
     - Data integrity and database safety
     - Complexity and maintainability
     - Code bloat and unnecessary additions
     - Test coverage adequacy
     - API contract compliance
     - Error handling and edge cases
     - Accessibility (where applicable)
     - Documentation completeness
     - Dependency safety (new packages evaluated)
     - Breaking changes to existing flows
     - Plan adherence (does the code match what was planned?)
  2. Each agent produces findings categorized by priority:
     - **P1 (Critical):** Must fix before merge. Security holes, data integrity risks, broken core flows.
     - **P2 (Important):** Should fix. Performance regressions, architecture drift, missing tests.
     - **P3 (Minor):** Nice to fix. Style issues, minor optimizations, documentation gaps.
  3. P1 findings trigger automatic fix attempts by the execution agent. The agent applies fixes and resubmits to the review agents. (This is the "my AI fixed the code before I even saw it" workflow that Kieran demonstrated.)
  4. The GM reviews all findings:
     - P1: Verifies fixes are adequate
     - P2: Decides which to address now vs. defer (with documented rationale)
     - P3: Addresses at discretion
  5. If P1 findings persist after agent fix attempts, escalate to Andrey Galko (Engineering Lead) for assessment.
- **Output:** Review-cleared PR with all P1 findings resolved, P2/P3 triaged
- **Criteria for completion:** Zero unresolved P1 findings. All P2/P3 findings have been reviewed by GM and either addressed or explicitly deferred with rationale.
- **Why 40% of time:** Review is where quality is enforced. Fourteen specialized reviewers catch what any single reviewer would miss. This step is what makes "99% AI-written code" safe to ship.

### Step 4: Compound (10% of total cycle time)
- **Responsible party:** AI agent + Product GM
- **Input:** Review-cleared PR, all review findings, and the implementation experience
- **Process:**
  1. **Document learnings:** Create or update entries in docs/solutions/ that capture:
     - What problem was solved
     - What approach worked (and what didn't, if the agent tried alternatives)
     - Key architectural decisions and their rationale
     - Any patterns discovered that apply beyond this specific feature
  2. **Update CLAUDE.md:** Add any new conventions, constraints, or preferences discovered during the cycle. Examples: "Always use X pattern for Y type of query," "This API has a rate limit of Z — batch accordingly."
  3. **Extract reusable patterns:** If the implementation produced a pattern that could apply to other products or future features, extract it into a shareable form. Flag it for the cross-GM knowledge feed (#engineering-learnings Slack channel).
  4. **Update review agent configuration:** If any review agent produced false positives or missed something important, update its configuration for next cycle.
  5. **GM verification:** The GM reviews the compound artifacts to ensure they're accurate and useful — not just checkbox compliance but genuine knowledge capture.
- **Output:** Updated docs/solutions/ entries, CLAUDE.md updates, extracted patterns, review agent configuration changes
- **Criteria for completion:** At least one compound artifact produced. GM has verified the artifacts are accurate and useful.
- **Why 10% of time:** This step is what makes it "compound" engineering, not just "AI-assisted" engineering. Without it, each feature cycle starts from scratch. With it, the system gets measurably smarter — the next similar feature takes 50% less time because the agent already knows the patterns, pitfalls, and conventions.

### Step 5: Merge and Deploy
- **Responsible party:** Product GM
- **Input:** Review-cleared PR with compound artifacts
- **Process:**
  1. GM performs final review of the complete PR (code + compound artifacts)
  2. GM merges to main/production branch
  3. Deployment follows product-specific CI/CD pipeline
  4. GM verifies the feature works in production against the success criteria from the plan
- **Output:** Feature live in production
- **Criteria for completion:** Feature is deployed, success criteria from plan.md are verified in production, no rollback within 48 hours

## Execution Model

- **Sequential dependencies:** Step 1 (Plan) → Step 2 (Work) → Step 3 (Review) → Step 4 (Compound) → Step 5 (Merge)
- **Parallel stages:** Within Step 3 (Review), all 14 review agents run in parallel (security, performance, architecture, data integrity, complexity, bloat, etc.). Multiple feature cycles can run concurrently across different git worktrees — a GM may have 4-5 features in different stages simultaneously.
- **Convergence point:** Step 3 (Review) is where all 14 agent findings converge. The GM triages P1/P2/P3 findings and decides what to fix before proceeding to Step 4.
- **Blocking gate:** Code Merge Gate between Step 4 (Compound) and Step 5 (Merge). Blocks on: test failures, unresolved P1 findings, missing compound artifact.
- **GM variation:** Each GM runs the same loop but with different tooling — Kieran (plan-first/Claude Code), Danny (Droid CLI), Naveen (Linear-centric/Codex), Yash (parallel Claude+Codex). The loop structure is standard; the execution tools are GM-autonomous.

## Feedback Loops

- **Compound → Plan:** Each cycle's docs/solutions/ entries and CLAUDE.md updates directly inform the next cycle's Plan step. The planning agent reads prior solutions when researching the codebase.
- **Review → Reviewer Config:** When review agents repeatedly flag the same pattern, the GM adds it to the reviewer's checklist. Kieran's `@kieran-rails-reviewer` evolves from discovered issues.
- **Cross-GM Knowledge Feed:** When one GM's compound step produces a generalizable solution, it's auto-posted to #engineering-learnings for other GMs to voluntarily adopt.
- **Gate Metrics → Gate Criteria:** Monthly review of rollback rate (target: <5%). If exceeded, gate criteria or review agent config needs adjustment.

## Quality Gate

**[Code Merge Gate](../gates/code-merge.md)**

Applied between Step 3 (Review) and Step 5 (Merge and Deploy). The gate enforces:

- **Tier 1 (blocking):** All tests pass, P1 findings resolved, plan adherence verified, core flows unbroken
- **Tier 2 (blocking):** At least one compound artifact produced, all P2/P3 findings triaged by GM
- **Tier 3 (advisory):** Performance impact, architecture alignment, dependency changes flagged for GM awareness

Target: 95% of PRs passing this gate should ship without requiring rollback within 48 hours.

GM override: GMs can override Tier 2 failures with documented rationale (e.g., emergency hotfix where compound step is deferred to a follow-up).

## Stranger Test

**Could someone with zero context execute this workflow from this spec alone?**

Yes, with these prerequisites:

1. **Repository access and structure:** A new GM needs access to the product's git repository, understanding of the branching strategy, and familiarity with the docs/solutions/ and CLAUDE.md file locations. These are standard across all four products.
2. **Agent tooling setup:** The compound engineering plugin must be installed and configured. Each GM has their preferred tooling (Claude Code, Codex, Droid CLI) — the new GM needs one working agent setup. Andrey Galko (Engineering Lead) can onboard.
3. **Review agent configuration:** The 14 review agents are pre-configured per product. A new GM inherits the existing configuration and adapts over time through Step 4 (Compound).
4. **Plan writing skill:** Writing a good plan.md is the hardest skill to transfer. New GMs should review 3-5 recent plans from other GMs to understand the expected depth and structure. The plan template (objectives, architecture, steps, success criteria, risks, prior solutions) is explicit, but judgment about what constitutes "thorough enough" develops with practice.
5. **Existing codebase knowledge:** The agent researches the codebase during planning, but the GM needs enough context to evaluate whether the agent's plan is sensible. New GMs should spend their first week reading existing docs/solutions/ entries and CLAUDE.md to build this context.

**Verdict:** A technically competent person familiar with software development could follow this spec to ship a feature. The compound engineering methodology is well-documented externally (12K+ GitHub stars), and the internal tooling is standard. The main gap is plan quality judgment, which the review step (14 agents + escalation to Andrey) mitigates.

## Iteration Protocol

This workflow is self-compounding by design — the Compound step (Step 4) is the iteration mechanism built into every cycle. Beyond per-cycle compounding:

1. **docs/solutions/ growth:** Each cycle adds to the institutional knowledge base. Track the number of docs/solutions/ entries per product per quarter. A product with a growing solutions library is a product that's compounding. A product with stale docs is a red flag.

2. **Cycle time tracking:** Measure total time from PRD to production for each feature. As the knowledge base grows, cycle time for similar-complexity features should decrease. If it doesn't, the Compound step isn't producing useful artifacts.

3. **Review agent false positive rate:** Monthly, each GM reviews whether review agents are producing useful findings or generating noise. Agents with high false-positive rates get their criteria tightened. Agents that consistently miss real issues get their scope expanded.

4. **Cross-GM knowledge transfer:** When one GM's compound artifacts are useful to another GM's product, flag and share via #engineering-learnings. Monthly "engineering show-and-tell" where GMs demo their best workflows reinforces this.

5. **Plan quality assessment:** Quarterly, Andrey reviews a sample of plans across all GMs to assess quality trends. Are plans getting more detailed? Are they referencing prior solutions? Are success criteria testable?

6. **Rollback analysis:** Every production rollback triggers a root cause analysis. Was the plan insufficient? Did review agents miss something? Was the compound knowledge that would have prevented this gap not yet captured? Findings feed back into the specific step that failed.
