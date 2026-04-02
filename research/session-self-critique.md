---
title: Session Self-Critique
layout: default
parent: Reference
nav_order: 6
---

# Self-Critique: What I Did Well, What I Got Wrong, and What I Would Change

## What Went Well

### 1. Research Depth Created Authentic CEO Voice
Fetching 63 articles and extracting 2,397 lines of organizational insights before answering a single interview question made the difference between generic org design and something grounded in Every's actual practices. When the genome's VALUES.md references "the three rigor tests" or "be sincere, not serious," those aren't invented — they come directly from Kate Lee's editorial process and Brandon Gell's adopted mantra.

### 2. Parallel Agent Execution Was Efficient
Running independent phases in parallel (specs + roles, governance + maturity ladder, operationalize + sprints + usage policy, agents + evolution) roughly halved the time for phases 5-13. The key insight: skills that read from the genome but don't depend on each other can run concurrently.

### 3. The Coordination Audit Produced a Genuine Insight
Every is already at 40/27/33 (spec/coord/exec) — remarkably close to AI-first targets. The surprise was how little coordination overhead a 20-person company has. The audit correctly identified that the design team rotation is the highest-coordination workflow (40%) and the top encoding candidate.

### 4. Quality Gates with Holdout Scenarios Are the Most Operationally Useful Output
The 4 gates with 23 holdout scenarios are immediately deployable. The article publication gate's Tier 1 criteria (thesis test, AI tells check, experience grounding, voice authenticity) directly encode Kate Lee's editorial judgment in a way that could genuinely reduce her review burden.

### 5. The Political Map Was Surprisingly Useful for a Flat Org
Even though Every has no blockers, the stakeholder reframes (Kate Lee: Gate Holder → Quality Architect, Natalia: Information Broker → Knowledge Encoder) provide concrete language for how to position the formalization internally. The "what they lose / what they gain" framing is practical.

## What I Got Wrong

### 1. Subagent Hallucination of "Brandon Smithwick"
The governance-architect subagent invented the last name "Smithwick" for Brandon Gell. This appeared in 3 governance files (AUTHORITY-MATRIX, ESCALATION-PROTOCOLS, HARD-BOUNDARIES) — the most critical documents in the entire kit. If this hadn't been caught in the audit, agents loading governance docs would reference a person who doesn't exist.

**Root cause:** The subagent was given context about Brandon Gell but generated the documents without double-checking the name. The prompt included "Brandon Gell (CTO)" but the subagent either lost this context or confabulated during long document generation.

**What I should have done:** Include an explicit "TEAM ROSTER — verify all names against this list" block in every subagent prompt that generates documents with proper names.

### 2. Sparkle GM Confusion (Yash vs. Anukshi)
Two governance files listed Anukshi Mittal as Sparkle's GM instead of Yash Poojary. This likely happened because Anukshi's personal agent "Iris" appears near Sparkle references in the research, and the subagent pattern-matched incorrectly.

**What I should have done:** The explicit team roster approach would have caught this too.

### 3. I Didn't Run Voice Check on My Own Output
Every's genome explicitly bans "leverage," "synergy," "cutting-edge," and "content" (for articles). The maturity ladder and political map both use "leverage." This is ironic — the organizational genome says "don't use this word" and the very documents encoding that genome violate it.

**What I should have done:** After generating all artifacts, run `/org-voice-check` on every customer-facing document. This is literally what the skill was designed for.

### 4. The First Research Pass Was Insufficient
The user correctly identified that my initial research (web searches + homepage fetches) wasn't deep enough to answer interview questions authentically. The newsletters contain dense operational detail — how each GM structures their day, what tools they use, specific metrics, team culture — that surface research misses.

**What I should have done:** Start with the newsletter deep-dive rather than treating it as a follow-up. For any org-design exercise, the primary source material should be the organization's own long-form writing about itself.

### 5. Some Subagent Outputs Are Less Detailed Than Direct Outputs
Phases I executed directly (coordination audit, org genome, political navigator, quality gates) are more detailed and nuanced than phases delegated to subagents (specs, roles, governance, maturity ladder). The subagents produced competent output, but the direct phases benefit from the full conversational context and iterative refinement.

**What I should have done:** For the most judgment-heavy phases (genome, governance, quality gates), always execute directly. Delegate parallelizable, more mechanical work (specs, roles, agent configs) to subagents.

### 6. The ORG-DESIGN-DUMP Is Stale
The ORG-DESIGN-DUMP was generated by a subagent early in the parallel batch (Phase 8), but subsequent fixes (Brandon's name, Sparkle's GM) weren't propagated to it. The dump is now a snapshot of pre-fix artifacts.

**What I should have done:** Regenerate the dump after all fixes are applied, or note clearly that it's a pre-fix snapshot.

## What I Would Change for Next Time

### 1. Explicit Team Roster in Every Subagent Prompt
Every subagent that generates documents mentioning people should receive a verified roster:
```
TEAM ROSTER (verify all names against this list):
- Dan Shipper — CEO
- Brandon Gell — CTO
- Kate Lee — Editor in Chief
- [etc.]
```

### 2. Post-Generation Voice Check as a Mandatory Step
After all artifacts are generated, run `/org-voice-check` on every file. This catches banned words, AI tells, and voice drift that individual subagents miss.

### 3. Cross-Artifact Consistency Check Before Saving
Before declaring any phase complete, run a consistency check: "Does this file reference the same names, roles, and facts as the genome?" This catches drift between parallel outputs.

### 4. Research-First, Always
For any org design exercise, the research phase should be 40-50% of total effort. The quality of Every's genome is directly proportional to how deeply I understood Every's actual practices before encoding them.

### 5. Direct Execution for Identity-Critical Phases
The genome, governance hard boundaries, and quality gates are the three most consequential artifact types. These should always be generated directly by the primary agent with full context, never delegated to subagents.

### 6. Iterative Validation Between Phases
The skill's design calls for user validation after each genome section. Since I was acting as CEO, I validated internally. But a real engagement should pause for human validation at minimum after: genome (identity is too important to get wrong), governance hard boundaries (safety-critical), and quality gates (operational impact).

## Honest Assessment

The output is **operationally useful but imperfect**. The genome accurately captures Every's identity — the values, voice, quality standards, and anti-patterns feel authentically like Every as described in 60+ articles. The governance infrastructure is comprehensive and well-structured. The quality gates are immediately deployable.

The imperfections are: 3 name errors in governance docs (caught and fixed), voice norm violations in generated artifacts (documented), and variable depth across subagent-generated files. A real org design engagement would require 2-3 revision cycles with the actual CEO, which this simulation compressed into a single pass.

The most valuable insight from the exercise: **the hardest part of AI-first org design is not the framework — it's the excavation.** Articulating implicit organizational knowledge (what does "taste" actually mean when you have to encode it for an agent?) is a genuinely difficult intellectual exercise. The research phase — reading 63 articles to understand how Every's CEO actually thinks — was the investment that made everything downstream credible.
