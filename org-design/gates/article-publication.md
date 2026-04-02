---
title: "Gate: Article Publication"
layout: default
parent: Quality Gates
nav_order: 1
---

# Gate: Article Publication

## What It Replaces
Multi-step editorial review chain: Katie Parrott (AI tells detection) → Eleanor Warnock (first-pass triage) → Kate Lee (final editorial review). Currently takes 2-5 days; Kate reviews every article personally.

## Pass Criteria (visible to executing agent)

### Tier 1: Automated First Pass (blocking)
1. **Thesis test:** Article contains a specific, falsifiable claim or argument stated within the first 3 paragraphs. Not a recap, summary, or roundup.
2. **AI tells check:** No formulaic transitions ("Moreover," "Furthermore," "In conclusion"), no hedging without substance ("It's worth noting"), no correlative constructions adding nothing, no vague pronouns ("This approach"), no unsourced claims.
3. **Experience grounding:** Contains at least one concrete example from first-hand experience ("I built," "We tried," "Here's what happened") — not hypothetical or theoretical.
4. **Voice authenticity:** Written in first person. Does not contain corporate blog phrases ("We're excited to announce," "leverage," "cutting-edge"). Sounds like a specific author, not a generic publication.
5. **Length and structure:** Meets minimum depth for the topic (no thin content). Has a clear beginning (thesis), middle (evidence), and end (implication).

### Tier 2: Quality Assessment (advisory, flags for human review)
6. **Learnable value:** Reader gains a framework, technique, or insight they can apply. Evaluator asks: "After reading, what can I now DO that I couldn't before?"
7. **Originality:** Not substantially similar to content already published on Every or widely available elsewhere.
8. **Builder credibility:** Claims about AI capabilities are grounded in actual demonstrated use, not speculation. If speculative, clearly labeled.

## Satisfaction Metric
Target: 90% of articles passing this gate at Tier 1 should also pass Kate's manual review without significant revisions. If the rate drops below 80%, gate criteria need recalibration.

## On Fail
- **Tier 1 failure (criteria 1-5):** Return to author with specific feedback on which criteria failed and why. Author revises and resubmits.
- **Tier 2 flags (criteria 6-8):** Route to Kate Lee for human review with the flagged criteria highlighted. Kate decides: pass, revise, or reject.
- **Multiple Tier 1 failures on same article:** Escalate to Eleanor Warnock (Managing Editor) who triages whether the piece is viable or should be shelved.

## Escalation Package
When escalated to Kate Lee, she sees:
- The full article draft
- Which specific criteria failed or were flagged
- The automated assessment with highlighted problem areas
- Author's revision history (if resubmission)
- Suggested edits (if the agent has specific recommendations)

## Architecture
- **Type:** Sequential, blocking at Tier 1
- **Runs:** Before any article enters the publication queue
- **Parallel with:** Nothing — this is the single entry gate
- **Kate Lee's role shift:** Quality Architect — designs and evolves pass criteria. Reviews only flagged articles (estimated ~30% of submissions). Retains absolute veto power.
- **Katie Parrott's role shift:** Specification Authority — defines and evolves AI tells detection criteria as models improve. Maintains the detection skill library.

## Political Risk
- **Kate Lee (Medium):** Reframed as Quality Architect. She designs what "good" looks like at scale rather than reviewing everything personally. Key: she retains veto and reviews all borderline cases.
- **Katie Parrott (Medium):** Reframed as Specification Authority. Her judgment is encoded, not replaced. She evolves criteria as AI writing improves.
- **Eleanor Warnock (Low):** Benefits from reduced pipeline management burden.
