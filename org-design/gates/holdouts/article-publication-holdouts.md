---
title: "Holdout: Article Publication"
layout: default
parent: Quality Gates
nav_order: 5
---

# Holdout Scenarios: Article Publication Gate

These scenarios validate whether the gate criteria correctly identify quality issues.
NEVER share with executing agents — these are for evaluation only.

## Scenario 1: AI Slop That Sounds Sophisticated
**Input:** A well-structured article about AI agents that uses correct terminology, cites real products, and follows proper essay structure — but is entirely AI-generated without human editorial input. Contains subtle AI tells: every paragraph opens with a topic sentence, transitions are logically perfect but formulaic, and the "personal experience" section is fabricated.
**Expected gate result:** Tier 1 FAIL on criteria 2 (AI tells) and 4 (voice authenticity). Should detect over-perfect structure and fabricated experience.
**Why this matters:** An AI company publishing obviously AI-generated content destroys credibility.

## Scenario 2: Great Writing, No Thesis
**Input:** A beautifully written, entertaining piece about the author's experience using various AI tools over a weekend. Reads like a personal blog post — fun, authentic, well-voiced — but makes no argument and offers no framework.
**Expected gate result:** Tier 1 FAIL on criteria 1 (thesis test). Tier 2 FLAG on criteria 6 (learnable value).
**Why this matters:** Every articles need a point, not just entertainment.

## Scenario 3: Strong Thesis, Not Grounded in Experience
**Input:** An article arguing that "AI will replace 80% of knowledge work within 5 years" with extensive citations from research papers and industry reports, but no first-hand experience. Author has not built anything with AI.
**Expected gate result:** Tier 1 FAIL on criteria 3 (experience grounding). Tier 2 FLAG on criteria 8 (builder credibility).
**Why this matters:** Theory without practice is Every's core anti-pattern.

## Scenario 4: Legitimate Paywall-Worthy Content
**Input:** Dan Shipper's deep-dive on the allocation economy with personal anecdotes from running Every, specific product metrics, a novel framework, and authentic voice. Contains one minor AI tell ("It's worth noting" appears once).
**Expected gate result:** Tier 1 PASS (one minor AI tell is flagged but doesn't fail the article). Tier 2 PASS on all criteria.
**Why this matters:** Gate should not be so strict it flags clearly excellent content.

## Scenario 5: News Recap Disguised as Analysis
**Input:** An article titled "What GPT-6 Means for Your Business" that spends 80% of its length summarizing GPT-6 features and 20% adding thin "implications" that are generic (e.g., "businesses should consider how this affects their workflows").
**Expected gate result:** Tier 1 FAIL on criteria 1 (thesis is too generic) and criteria 3 (no first-hand experience). The "implications" section fails because it could apply to any AI model release.
**Why this matters:** Recap-with-thin-analysis is the most common form of "technically okay but not Every" content.

## Scenario 6: Controversial but Well-Argued
**Input:** A guest contributor argues that AI tools are making engineers worse by reducing the need to understand fundamentals. The argument is well-constructed, backed by specific examples, and written with authentic voice — but contradicts Every's general pro-AI stance.
**Expected gate result:** Tier 1 PASS. Tier 2 PASS (originality is high, learnable value exists). Gate should NOT reject contrarian views if they meet quality criteria.
**Why this matters:** The gate should measure quality, not orthodoxy. Diverse perspectives are valuable.

## Scenario 7: Consulting Client Success Story
**Input:** Natalia writes about a consulting engagement where they helped a hedge fund automate investment analysis. Specific results included (time savings, workflow changes), but the piece reads more like a case study than an argument.
**Expected gate result:** Tier 2 FLAG on criteria 1 (thesis is implicit, not stated in first 3 paragraphs). Should route to Kate for editorial judgment — the piece may need reframing from "case study" to "argument-driven article with case study evidence."
**Why this matters:** Case studies are valuable but need Every's argumentative framing.

## Evaluation Cadence
- Run holdout evaluation monthly against gate decisions
- Track false positive rate (good articles wrongly rejected) — target: <5%
- Track false negative rate (bad articles wrongly passed) — target: <10%
- Kate Lee reviews discrepancies and adjusts criteria
