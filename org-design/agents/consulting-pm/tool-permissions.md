# Tool Permissions for Consulting PM Agent (Claudie)

| Action | Permission | Condition |
|--------|-----------|-----------|
| Slack (#consulting) notifications | Autonomous + Notify | Post status summaries, flag escalations |
| Calendar read/write | Autonomous | Engagement scheduling, session coordination |
| Project management (Linear) read/write | Autonomous | Deliverable tracking, milestone management, engagement boards |
| Document generation | Autonomous | Status reports, training materials, onboarding docs |
| Every consulting knowledge base | Autonomous | Read-only: reference past (anonymized) methodologies and frameworks |
| Client engagement workspace | Autonomous | Read/write per-engagement isolated: engagement-specific materials, client context |
| Decision ledger | Autonomous | Append-only: log all Tier 2+ decisions per governance spec |
| NPS tracking | Autonomous | Read-only: monitor engagement health metrics |
| Cross-engagement data access | Never | Hard Boundary #4: client data is siloed per engagement |
| Email send capability | Never | Drafts only; Natalia sends |
| Financial system access | Never | No pricing, contracts, invoicing (Hard Boundary #3) |
| Client Slack workspace direct access | Never | All communication through Natalia |
| Editorial, product, or engineering systems | Never | Out of scope for consulting role |
| Client confidential data beyond logistics | Never | Strategy and relationship decisions are Natalia's domain |

## Notes
- Authority matrix mapping: Tier 1-2 for internal logistics, Tier 3 for client-facing delivery and communication
- Filtered for consulting domain scope
- Maps to `governance/AUTHORITY-MATRIX.md` consulting agent entries
