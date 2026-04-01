---
name: org-voice-check
description: "Review content against organizational voice norms before publishing. Use before publishing articles, documentation, external communications, or any content visible to people outside the organization."
allowed-tools: Read
context: fork
agent: general-purpose
---
<!-- generated-by: ai-first-kit v1.4.2 -->

# Voice Check

Review content against organizational voice norms.

## Process

1. Read the voice specification:
   `$HOME/.ai-first-kit/projects/every/genome/00-identity/VOICE.md`

2. Identify the **target channel** for this content (newsletter, social, consulting, product copy, legal).
   Apply the formality gradient from VOICE.md.

3. Check against voice criteria:

   ### Words We Use
   Scan for presence of Every's vocabulary: "allocation economy," "compound engineering," "taste," "ship," "builder," specific tool names, first names.

   ### Words We Never Use
   Scan for banned vocabulary: "leverage," "synergy," "cutting-edge," "best-in-class," "we're excited to announce," "democratize," "disrupt," "content" (for articles), "users" (for readers/subscribers). Flag every occurrence.

   ### AI Tells Detection
   Check for: "Moreover," "Furthermore," "In conclusion," "It's worth noting," correlative constructions ("Not only X, but also Y"), vague pronouns ("This approach"), hedging without substance, unsourced claims, lists in arbitrary order. Flag every occurrence.

   ### Formality Match
   Does the tone match the target channel per the gradient table?

   ### Three Rigor Tests (Articles only)
   (1) Articulates something true — specific, falsifiable claim
   (2) Offers learnable value — reader gains applicable insight
   (3) Sounds authentically like the writer — not interchangeable

4. Produce a **pass/fail report**:

   ```
   ## Voice Check Report

   **Target channel:** [channel]
   **Expected formality:** [level from gradient]

   ### Results
   - [ ] No banned words: {PASS/FAIL — list violations}
   - [ ] No AI tells: {PASS/FAIL — list violations}
   - [ ] Formality matches channel: {PASS/FAIL — mismatches}
   - [ ] Every vocabulary present: {PASS/FAIL — suggestions}
   - [ ] Rigor tests (if article): {PASS/FAIL per test}

   ### Specific Fixes
   {For each failure, exact fix with before/after}

   **Overall:** PASS / NEEDS REVISION
   ```

## Rules
- Every failure must include a specific fix, not just a flag
- Check the FULL content, not just the first few paragraphs
- The voice check is about TONE and AUTHENTICITY, not factual accuracy
