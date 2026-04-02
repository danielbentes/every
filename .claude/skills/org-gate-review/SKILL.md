---
name: org-gate-review
description: "Self-review against a specific quality gate before presenting work. Use before submitting code for review, publishing content, creating releases, or presenting any work output."
argument-hint: "[gate-name]"
allowed-tools: Read
context: fork
agent: general-purpose
---
<!-- generated-by: ai-first-kit v1.4.2 -->

# Gate Self-Review

Run a structured self-review against a quality gate's pass criteria.

## Process

1. Determine which gate to review against:
   - If `$ARGUMENTS` provided, use it as the gate name (e.g., `article-publication`)
   - If no argument, read the gate index and suggest the most relevant gate:
     `org-design/gates/INDEX.md`

2. Read the gate file:
   `org-design/gates/$ARGUMENTS.md`

3. Extract the **Pass Criteria** section from the gate file.

4. For EACH criterion, evaluate the current work:

   ```
   ## Gate Review: [Gate Name]

   | # | Criterion | Status | Evidence |
   |---|-----------|--------|----------|
   | 1 | [criterion text] | PASS/FAIL | [specific evidence or violation] |
   | 2 | [criterion text] | PASS/FAIL | [specific evidence or violation] |
   ...

   **Overall:** PASS (all criteria met) / FAIL (N criteria failed)
   ```

5. For each FAIL:
   - Identify the specific fix needed
   - If the fix is within your capability, describe it
   - If the fix requires a different skill/role, note which one

6. If all criteria PASS: "Gate [name] passed. Ready for the next stage."
   If any criteria FAIL: "Gate [name] failed on N criteria. Fixes needed before proceeding."

## Available Gates
- `article-publication` — editorial quality (thesis, AI tells, voice, rigor tests)
- `code-merge` — compound engineering (tests, P1 findings, plan adherence, compound artifact)
- `consulting-deliverable` — consulting quality (experience grounding, confidentiality, hands-on)
- `social-media-publication` — social media (voice, thesis capture, accuracy)

## Rules
- NEVER read holdout files (`gates/.holdouts/`) — they test agents, not for agent consumption
- Review against the VISIBLE pass criteria only
- Every PASS must cite specific evidence (not just "looks good")
- Every FAIL must include a specific fix
