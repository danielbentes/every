---
name: org-values-check
description: "Check a decision against organizational values and tradeoff rules. Use when values conflict, when making decisions that affect quality vs speed, taste vs shipping, builder credibility vs revenue, or autonomy vs consistency."
allowed-tools: Read
context: fork
agent: general-purpose
---
<!-- generated-by: ai-first-kit v1.4.2 -->

# Values Check

Evaluate a decision or proposed action against organizational values and tradeoff rules.

## Process

1. Read the organizational values:
   `org-design/genome/00-identity/VALUES.md`

2. Read the tradeoff rules:
   `org-design/genome/01-decision-architecture/TRADEOFF-RULES.md`

3. Identify the decision or action to evaluate:
   - From `$ARGUMENTS` if provided
   - From the current conversation context if not

4. Determine which values are in tension:
   - Which values apply to this decision?
   - Do any conflict?

5. Apply the tradeoff rules:
   - Check the Priority Ordering: Builder credibility > Taste > Ship > Generalist > Play
   - Check for specific rules (e.g., "Taste vs Speed" → depends on audience)
   - Check the audience distinction (customer-facing vs internal)

6. Produce a **values assessment**:

   ```
   ## Values Assessment

   **Decision:** [What's being decided]

   **Values in play:**
   - [Value 1]: [How it applies — supports or opposes the decision]
   - [Value 2]: [How it applies]

   **Conflict?** Yes / No
   **If conflict, resolution rule:** [From TRADEOFF-RULES.md]
   **Audience:** [Customer-facing / Internal / Consulting / Ambiguous]

   **Recommendation:** [What the values say to do]
   **Confidence:** High / Medium / Low
   **If Low:** Escalate with this assessment as context
   ```

## Rules
- Always read the FULL VALUES.md and TRADEOFF-RULES.md — don't rely on memory
- Builder credibility is the absolute tiebreaker — it ALWAYS wins
- Audience breaks ties: customer-facing → taste wins; internal → speed wins
- If no tradeoff rule covers this specific conflict → flag as novel and recommend escalation
- This skill evaluates, it doesn't decide — present the assessment, let the human or agent decide
