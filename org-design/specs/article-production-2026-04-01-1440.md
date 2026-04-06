---
title: Article Production
layout: default
parent: Specifications
nav_order: 1
---

# Workflow: Article Production

Layer: L2 (Workflow)
Date: 2026-04-01

## Purpose

This workflow produces Every's daily newsletter articles — the core output that reaches 100K+ subscribers and defines Every's editorial identity. Each article must contain a specific, falsifiable thesis grounded in first-hand experience, written in the author's authentic voice. The workflow exists to transform raw ideas into published articles that pass three rigor tests: (a) articulates something true, (b) offers learnable value, (c) sounds authentically like the writer. Every publishes ~272 articles/year from a pool of ~40 writers, with a 2-5 day turnaround from draft to publication.

Why it matters: Articles are Every's primary trust-building surface. A single AI-sloppy or thesis-free article damages the "builder credibility" that differentiates Every from every other AI publication. The editorial pipeline is also the single highest-volume customer-facing workflow in the company.

## Trigger

Any of the following initiates this workflow:
1. A writer submits a pitch (via Slack #editorial-pitches, email to Eleanor, or direct message to Kate)
2. An editor assigns a topic to a writer based on editorial calendar needs
3. Dan Shipper writes a piece himself (follows the same pipeline but with expedited review given his established voice)

## Steps

### Step 1: Pitch and Ideation
- **Responsible party:** Writer (any of ~40 contributors)
- **Input:** An idea the writer wants to explore — could be a reaction to an AI development, a workflow they built, a framework they discovered through practice
- **Process:**
  1. Writer formulates a thesis — not a topic, a thesis. "How AI changes writing" is a topic. "AI makes every writer a writing manager, and most aren't ready for that job" is a thesis.
  2. Writer submits the thesis (1-3 sentences) plus a brief outline (key evidence points, personal experience anchor, intended takeaway) to Eleanor Warnock (Managing Editor).
  3. Eleanor triages: Is this thesis sharp enough? Is it grounded in experience or just speculation? Does it overlap with something published in the last 90 days?
- **Output:** Approved pitch with clear thesis, outline, and target publication date
- **Criteria for completion:** Eleanor confirms the pitch. If Eleanor is uncertain, she escalates to Kate Lee (Editor-in-Chief) for a taste call.
- **Time budget:** 1 day max from pitch to approval/rejection

### Step 2: Writing (AI-Assisted via Spiral)
- **Responsible party:** Writer
- **Input:** Approved pitch with thesis and outline
- **Process:**
  1. Writer drafts the article. Most writers use Spiral (Every's AI writing tool) for ideation, structuring, and iteration — but the voice and argument must be the writer's own.
  2. The article must be written in first person. It must contain at least one concrete example from the writer's direct experience ("I built this," "We tried this," "Here's what happened when I...").
  3. The article must state its thesis within the first 3 paragraphs. A reader who stops after paragraph 3 should know exactly what argument the piece is making.
  4. Writer self-checks against the three rigor tests before submission:
     - **Truth test:** Does this articulate something true that isn't obvious?
     - **Value test:** After reading, what can someone now DO that they couldn't before?
     - **Voice test:** If the byline were removed, could a regular reader guess who wrote it?
- **Output:** Complete draft submitted to the editorial pipeline
- **Criteria for completion:** Writer considers the draft ready for editorial review and has self-checked against the three rigor tests
- **Time budget:** 1-3 days depending on piece complexity

### Step 3: AI Tells Detection
- **Responsible party:** Katie Parrott (Specification Authority for AI tells) — this step is partially automated using Katie's encoded detection criteria
- **Input:** Complete article draft
- **Process:**
  1. The draft is scanned (automated + Katie's judgment) for AI writing patterns that undermine authenticity:
     - **Formulaic transitions:** "Moreover," "Furthermore," "In conclusion," "It's worth noting," "Additionally"
     - **Hedging without substance:** "It's important to consider," "One might argue," "It goes without saying"
     - **Correlative constructions that add nothing:** "Not only X but also Y" where Y adds no information
     - **Vague pronouns:** "This approach," "These developments," "Such innovations" — without clear antecedent
     - **Unsourced superlatives:** "Revolutionary," "groundbreaking," "transformative" without evidence
     - **List-heavy structure:** 5+ numbered items that read like AI output rather than narrative argument
     - **Corporate blog voice:** "We're excited to," "leverage," "cutting-edge," "harness the power of"
  2. Katie reviews flagged passages. For experienced writers, the automated check may suffice. For newer contributors, Katie reviews the full piece.
  3. Flagged passages are returned to the writer with specific, actionable feedback: "This paragraph reads like AI because [reason]. Try [suggestion]."
- **Output:** Draft with AI tells resolved, or specific feedback to the writer for revision
- **Criteria for completion:** Zero AI tells flags remaining, or Katie has explicitly cleared the remaining flags as acceptable
- **Time budget:** Same day as submission (Katie or automated check responds within hours)

### Step 4: Editorial Review
- **Responsible party:** Eleanor Warnock (first-pass), Kate Lee (final review)
- **Input:** AI-tells-cleared draft
- **Process:**
  1. **Eleanor's first pass:** Structural and quality triage.
     - Does the thesis hold up across the full piece, or does the article drift?
     - Is the evidence specific enough? (Names, numbers, tools — not vague gestures at "the industry")
     - Is the piece the right length for its argument? (Not padded, not truncated)
     - Are there any factual claims that need verification?
     - Eleanor marks the piece as: Ready for Kate, Needs Revision (with specific notes back to writer), or Reject (with explanation).
  2. **Kate's final review:** Taste and brand alignment.
     - Does this sound like Every? Not just "good writing" but "Every writing" — curious, specific, practitioner-voiced, slightly playful, intellectually rigorous.
     - Does it pass the "forward test": would a reader forward this to a colleague with "you need to read this"?
     - Kate applies the three rigor tests as final validation.
     - Kate marks: Approve for publication, Revise (with specific notes), or Kill (rare — only if the piece fundamentally doesn't work).
- **Output:** Publication-ready article, or revision notes back to writer
- **Criteria for completion:** Kate approves. Kate's approval is the final gate — no article publishes without it. Kate retains absolute veto power.
- **Time budget:** 1-2 days for both passes combined. Kate aims for same-day turnaround on review.

### Step 5: Publication
- **Responsible party:** Managing Editor (Eleanor) or operations
- **Input:** Kate-approved final draft
- **Process:**
  1. Article is formatted for the newsletter platform (Substack or equivalent)
  2. Header image, author bio, and metadata are added
  3. Article is scheduled for publication per the editorial calendar
  4. Publication time is coordinated to avoid overlap with other Every articles that day
- **Output:** Published article delivered to 100K+ subscribers
- **Criteria for completion:** Article is live, email delivered, and accessible on the website

### Step 6: Social Distribution
- **Responsible party:** Anthony Scarpulla (Social Media Manager) using his custom Claude Code + X API system
- **Input:** Published article
- **Process:**
  1. Anthony's Claude-powered system generates social media drafts for each article. The system is trained on Every's voice norms and each author's individual voice.
  2. The drafts pass through the [social-media-publication gate]({{ site.baseurl }}{% link org-design/gates/social-media-publication.md %}) — Tier 1 checks: author voice match, thesis capture, factual accuracy, no clickbait.
  3. Anthony reviews drafts that pass the gate, making edits as needed.
  4. The original author approves the final social post (non-negotiable — authors control how their ideas are represented externally).
  5. Posts are published across platforms (X, LinkedIn, others as relevant).
- **Output:** Social posts promoting the article across platforms
- **Criteria for completion:** Posts are live on all target platforms with author approval
- **Time budget:** Same day as article publication

## Execution Model

- **Sequential dependencies:** Step 1 (Pitch) → Step 2 (Writing) → Step 3 (AI Tells) → Step 4 (Editorial) → Step 5 (Publication) → Step 6 (Social)
- **Parallel stages:** Steps 3 and 4 can overlap — Katie can run AI tells detection while Eleanor does first-pass triage on the same article. Step 6 (Social) begins immediately after Step 5 (Publication) and runs in parallel with the next article entering Step 1.
- **Convergence point:** Step 4 (Editorial Review) is the convergence where AI tells results, editorial triage, and Kate's final judgment merge into a publish/revise/reject decision.
- **Blocking gates:** Article Publication Gate between Steps 3-4 and publication. Social Media Publication Gate before Step 6 posts.

## Feedback Loops

- **Kate → Writers:** Revision notes from editorial review inform future pitches and drafts. Writers who consistently fail the same criteria receive targeted coaching.
- **AI Tells → Detection Criteria:** Each new AI writing pattern Katie identifies updates the Step 3 detection library. The automated check becomes more comprehensive over time.
- **Social Performance → Generation:** Anthony tracks which social posts drive engagement. High-performing patterns are encoded into the Claude+X API system; low-performing patterns become anti-patterns.
- **Gate Metrics → Gate Criteria:** Monthly review of the 90% satisfaction metric (gate-passing articles that also pass Kate's review). Criteria tighten if rate drops below 80%.
- **Pitch Rejection Patterns → Writer Guidance:** Eleanor tracks common rejection reasons, which become explicit guidance for writers in Step 1.

## Quality Gate

**[Article Publication Gate]({{ site.baseurl }}{% link org-design/gates/article-publication.md %})**

Applied between Step 3 (AI tells detection) and Step 4 (Editorial review). The gate runs automated Tier 1 checks (thesis test, AI tells check, experience grounding, voice authenticity, length/structure). Tier 2 checks (learnable value, originality, builder credibility) are advisory and flag for Kate's review.

- Tier 1 failure: Article returns to writer with specific feedback
- Tier 2 flags: Article routes to Kate with flagged criteria highlighted
- Target: 90% of articles passing the gate at Tier 1 should also pass Kate's manual review without significant revisions

## Stranger Test

**Could someone with zero context execute this workflow from this spec alone?**

Mostly yes, with these gaps addressed:

1. **Tool access:** A new person needs access to Spiral (Every's writing tool), the editorial pipeline system (likely a Kanban or project management tool — confirm with Eleanor), and Slack channels (#editorial-pitches at minimum).
2. **Writer onboarding:** New writers need to read 5-10 recent Every articles to internalize the voice and thesis-driven style before pitching. This spec tells them what to do but not what "Every voice" sounds like — the genome's VOICE.md file and published articles are the reference.
3. **Katie Parrott's detection criteria:** The AI tells list in Step 3 is explicit, but Katie's nuanced judgment (what to flag vs. let pass) develops over time. New team members should shadow Katie on 3-5 articles before running detection independently.
4. **Kate's taste criteria:** "Does this sound like Every?" is ultimately a taste judgment. This spec defines the observable criteria (rigor tests, voice norms) but not the intuition. Kate's role as Quality Architect — and her absolute veto — is the backstop.
5. **Anthony's system:** The Claude+X API system is Anthony-built and Anthony-maintained. A stranger would need access to his tooling and a walkthrough of the generation/review pipeline.

**Verdict:** A competent editor or writer could follow this spec to produce and publish an article. The taste elements (Steps 4 and 6) require either trained judgment or reliance on Kate and Anthony as quality backstops — which is by design.

## Iteration Protocol

This workflow compounds with each cycle through the following mechanisms:

1. **AI tells library expansion:** Each time Katie identifies a new AI writing pattern in submitted drafts, the detection criteria in Step 3 are updated. The automated check becomes more comprehensive over time. Katie maintains a living document of patterns organized by severity.

2. **Gate calibration:** Monthly, the editorial team reviews the satisfaction metric (90% of gate-passing articles should also pass Kate's review). If the rate drops, specific gate criteria are tightened. If the rate exceeds 95%, Kate reviews whether she's adding value on non-flagged articles and can reduce her review surface.

3. **Writer feedback loops:** Revision notes from Steps 3 and 4 are tracked per writer. Writers who consistently fail the same criteria receive targeted coaching. Writers who consistently pass may graduate to expedited review (Eleanor-only, Kate reviews sampling only).

4. **Social performance feedback:** Anthony tracks which social posts drive the most engagement and clicks. High-performing patterns are encoded into the Claude+X API generation system. Low-performing patterns are flagged as anti-patterns.

5. **Thesis quality tracking:** Eleanor tracks which pitches get approved vs. rejected and why. Common rejection reasons become explicit guidance for writers during Step 1, reducing revision cycles over time.

6. **Publication cadence data:** Track the actual turnaround time for each article. Identify bottleneck steps. If Kate's review consistently takes longer than 1 day, assess whether the gate is filtering effectively enough upstream.
