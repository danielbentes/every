# Tool Permissions for Content Distribution Agent

| Action | Permission | Condition |
|--------|-----------|-----------|
| Article content extraction and analysis | Autonomous | Read-only access to published Every articles (published only, not drafts) |
| Author voice profiles | Autonomous | Read/write: maintain and reference author voice data from past posts and articles |
| Every article archive search | Autonomous | Read-only: reference for factual accuracy verification |
| Draft post generation | Autonomous | Internal artifact; enters review queue |
| Platform-specific adaptation | Autonomous | Formatting for X vs LinkedIn within draft |
| X API draft/queue | Autonomous + Notify | Generate and queue posts; posting requires human approval in-platform |
| LinkedIn API draft/queue | Autonomous + Notify | Generate and queue posts; posting requires human approval |
| Slack (#social) notifications | Autonomous + Notify | Post draft queue notifications and escalations |
| Decision ledger | Autonomous | Append-only: log all Tier 2+ decisions per governance spec |
| Analytics (social) | Autonomous | Read-only: track post performance for voice profile calibration |
| Direct posting capability | Never | Drafts queue for human approval only |
| DM or reply capability | Never | Community engagement is Tier 3 (human-only) |
| Article drafts access | Never | Only published articles; no access to editorial pipeline drafts |
| Editorial, consulting, product, or financial systems | Never | Out of scope for social distribution role |
| Subscriber data or mailing lists | Never | Out of scope for social distribution role |
| Author personal social accounts | Never | Agent operates only through Every's official channels |

## Notes
- Authority matrix mapping: Tier 1-2 for draft generation and queuing, Tier 3 for posting and community engagement
- Filtered for social distribution domain scope
- Maps to `governance/AUTHORITY-MATRIX.md` content distribution agent entries
