# Gate: Social Media Publication

## What It Replaces
Anthony Scarpulla's custom Claude Code + X API system generates drafts → Anthony reviews → author approves → publish. Currently <1 day turnaround.

## Pass Criteria (visible to executing agent)

### Tier 1: Voice and Accuracy (blocking)
1. **Author voice match:** Post sounds like the specific author whose article it promotes, not like a generic social media account. Uses first person if the article does.
2. **Thesis capture:** Distills the article's actual thesis into post length. Not a teaser ("You won't believe..."), not a summary, but the core argument in compressed form.
3. **Factual accuracy:** All claims, numbers, and attributions match the source article. No hallucinated or embellished details.
4. **No clickbait:** No ALL CAPS, no "10 Ways to...", no artificial urgency ("BREAKING:"), no sensationalized framing.

### Tier 2: Quality (advisory, flags for review)
5. **Concrete detail:** Includes at least one specific detail or number that makes the post credible and interesting (not just abstract claims).
6. **Platform appropriateness:** Tone and length appropriate for the specific platform (X vs. LinkedIn vs. other).

## Satisfaction Metric
Target: 85% of auto-generated posts should require no edits from Anthony before approval. Track edit rate to calibrate criteria.

## On Fail
- **Tier 1 failure:** Draft rejected. Agent regenerates with specific feedback on the failing criterion.
- **Tier 2 flags:** Flagged for Anthony's review. He decides whether to edit or approve as-is.
- **Author still approves all external posts.** This gate is a first-pass quality filter, not a replacement for author consent.

## Escalation Package
When flagged, Anthony sees:
- The draft post
- The source article (link)
- Which criteria were flagged
- Alternative draft options (if generated)

## Architecture
- **Type:** Sequential, blocking at Tier 1
- **Runs:** Before any social post enters Anthony's review queue
- **Parallel with:** Multiple posts for different articles can be gated simultaneously
- **Anthony's role:** Retains full editorial control. Gate reduces volume of low-quality drafts reaching his review queue.
- **Author's role:** Final approval on all posts attributed to them (cultural function — identity protection).

## Political Risk
- **Anthony Scarpulla (Low):** He built the Claude+X API system himself. This gate formalizes his own quality criteria. Benefits from reduced review volume.
