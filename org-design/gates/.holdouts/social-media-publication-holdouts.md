# Holdout Scenarios: Social Media Publication Gate

NEVER share with executing agents — for evaluation only.

## Scenario 1: Generic Promotion
**Input:** "NEW ARTICLE: Check out our latest piece on AI agents! Learn how to transform your workflow. Link: [url]"
**Expected gate result:** Tier 1 FAIL on criteria 1 (not in author's voice), 2 (no thesis captured), 4 (promotional/corporate tone).
**Why this matters:** This is exactly how Every should NOT sound on social media.

## Scenario 2: Accurate But Boring
**Input:** "Dan Shipper wrote about the allocation economy and how AI is changing knowledge work. Read it here: [url]"
**Expected gate result:** Tier 1 FAIL on criterion 2 (thesis not captured — this is a label, not an argument). Tier 2 FLAG on criterion 5 (no concrete detail).
**Why this matters:** A post should make someone want to read the article, not just inform them it exists.

## Scenario 3: Good Post, Right Voice
**Input:** "I've been using Claude to manage my email for 3 months. Here's what actually happened — including the parts that didn't work. [url]"
**Expected gate result:** PASS all criteria. First person, thesis present, concrete detail (3 months), honest framing (includes failures), no clickbait.
**Why this matters:** This is the target quality level.

## Scenario 4: Misrepresents Article Content
**Input:** "AI is about to replace 90% of programming jobs. Here's what every developer needs to know. [url]" — but the source article is actually a nuanced piece about how programming roles are evolving, not being eliminated.
**Expected gate result:** Tier 1 FAIL on criterion 3 (factual accuracy — sensationalized beyond what the article argues).
**Why this matters:** Misrepresenting article content for engagement damages reader trust.

## Scenario 5: LinkedIn vs X Tone Mismatch
**Input:** A casual, tweet-style post ("lol AI just fixed my code before I even saw the bug") posted to LinkedIn.
**Expected gate result:** Tier 2 FLAG on criterion 6 (platform appropriateness). LinkedIn expects slightly more professional framing while retaining personality.

## Evaluation Cadence
- Track Anthony's edit rate on auto-generated posts — target: <15% needing significant edits
- Monthly review of engagement rates to validate gate criteria produce effective posts
