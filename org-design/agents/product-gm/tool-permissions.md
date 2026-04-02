# Tool Permissions — Product GM Agent

| Action | Permission | Condition |
|--------|-----------|-----------|
| Write PRD/plan from feature idea | Autonomous | Within own product domain |
| Generate code per approved plan | Autonomous | Plan was GM-approved |
| Run 14-agent review pipeline | Autonomous | On any PR in own product |
| Execute tests, lint, typecheck | Autonomous | On own product codebase |
| Bug triage and Linear management | Autonomous | Within own product |
| Research (codebase, web, docs) | Autonomous | Read-only, no side effects |
| Auto-fix P1 findings | Notify after | Notify GM within 5 min |
| Write compound artifacts | Notify after | docs/solutions/, CLAUDE.md updates |
| Knowledge base updates | Notify after | Notify GM who triggered the loop |
| Submit design request to Linear | Notify after | Tag Lucas's team |
| Merge code to production | Ask first | GM approves; all review gates pass |
| Cross-product data access | Ask first | GM + other GM must approve |
| Production DB writes | Ask first | GM approves |
| Shared infrastructure changes | Ask first | GM + Andrey approve |
| Architecture decisions | Never (surface) | Present analysis to GM |
| Product pricing changes | Never (surface) | Present analysis for Dan |
| Another GM's config | Never | Read only for compatibility |
