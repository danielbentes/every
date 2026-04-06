---
title: Quality Gates
layout: default
nav_order: 6
has_children: true
---

# Quality Gates — Every Inc
Generated: 2026-04-01

## Gate Architecture Overview

```
Article draft → [article-publication gate] → Kate reviews flags → Publish
                    ↓ (Tier 1 fail)
                Author revises → resubmit

PR ready → [code-merge gate] → GM reviews Tier 3 flags → Merge
               ↓ (Tier 1-2 fail)
           Agent fixes → resubmit

Deliverable ready → [consulting-deliverable gate] → Natalia reviews flags → Client delivery
                         ↓ (Tier 1 fail)
                     Revise → resubmit

Social draft → [social-media-publication gate] → Anthony reviews → Author approves → Post
                    ↓ (Tier 1 fail)
                Agent regenerates
```

## Gates Summary

| Gate | Type | Blocking | Original Approver | New Role | Political Risk |
|------|------|----------|-------------------|----------|---------------|
| [article-publication]({% link org-design/gates/article-publication.md %}) | Sequential | Tier 1-2 blocking | Kate Lee (EIC) | Quality Architect — designs evolving criteria, reviews flags, retains veto | Medium |
| [code-merge]({% link org-design/gates/code-merge.md %}) | Sequential | Tier 1-2 blocking | Product GMs | Unchanged — gate formalizes existing review process | Low |
| [consulting-deliverable]({% link org-design/gates/consulting-deliverable.md %}) | Sequential | Tier 1-2 blocking | Natalia Quintero | Practice Architect — designs engagement framework, reviews flags | Medium |
| [social-media-publication]({% link org-design/gates/social-media-publication.md %}) | Sequential | Tier 1 blocking | Anthony Scarpulla + Author | Unchanged — gate is first-pass filter, humans retain all approval | Low |

## Holdout Scenarios
Located in `gates/.holdouts/` — separate from gate specs to prevent executing agents from seeing evaluation criteria.

| Gate | Holdout File | Scenarios |
|------|-------------|-----------|
| article-publication | [article-publication-holdouts]({% link org-design/gates/.holdouts/article-publication-holdouts.md %}) | 7 scenarios |
| code-merge | [code-merge-holdouts]({% link org-design/gates/.holdouts/code-merge-holdouts.md %}) | 6 scenarios |
| consulting-deliverable | [consulting-deliverable-holdouts]({% link org-design/gates/.holdouts/consulting-deliverable-holdouts.md %}) | 5 scenarios |
| social-media-publication | [social-media-publication-holdouts]({% link org-design/gates/.holdouts/social-media-publication-holdouts.md %}) | 5 scenarios |

## Approval Holder → Quality Architect Mapping

| Person | Old Role | New Role | What Changes |
|--------|----------|----------|-------------|
| Kate Lee | Reviews every article | Designs editorial criteria, reviews ~30% (flagged articles), retains absolute veto | Reviews less, designs more |
| Katie Parrott | Manual AI tells detection | Specification Authority — defines and evolves detection criteria | Judgment scales via criteria |
| Eleanor Warnock | First-pass pipeline management | Benefits from automated triage — focuses on writer development | Reduced coordination overhead |
| Product GMs | Review agent findings, merge decision | Same — gate formalizes existing process, adds compound artifact requirement | Minimal change |
| Natalia Quintero | Reviews all consulting deliverables | Practice Architect — designs engagement quality framework | Methodology scales |
| Anthony Scarpulla | Reviews all social drafts | Same — gate reduces low-quality drafts reaching him | Reduced review volume |

## Evaluation Schedule
- **Monthly:** Run holdout scenarios against gate decisions; track false positive/negative rates
- **Quarterly:** Gate criteria review by respective Quality Architects (Kate, Natalia, GMs)
- **Annual:** Full gate architecture review by Dan (CEO) and Brandon (CTO)
