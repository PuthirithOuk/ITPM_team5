# Approach comparison · Realtime Quiz

Sources: [project profile](project-profile.md), [scoring sheet](approach-scoring.csv)

| Approach   | Requirements | Sponsor control | First quiz | Two main risks | Fit |
|------------|--------------|-----------------|-----------:|----------------|-----|
| Waterfall  | Frozen in week 3 scope statement and WBS; changes need a formal change request | Strong: approved plan at week 3, then progress against baseline; single acceptance at the end | week 12 | 1. WebSocket or proxy problems found only at integration, too late to react. 2. UI misunderstandings surface only in the pilot week | Low (2.60): strong on governance, weak on uncertainty and feedback |
| Pure Scrum | Backlog reordered every sprint; no baseline | Sponsor sees a review every 2 weeks but has no gate to stop or re-plan; budget tracked only by velocity | week 5 (if the PO prioritises a thin end-to-end slice) | 1. First-time team drifts without a plan or an outside check. 2. Fixed pilot date and week-3 plan approval are not protected | Medium (3.70): strong on feedback and uncertainty, weak on governance |
| Hybrid     | Must list baselined at G1; order and detail inside the baseline are refined each sprint | Predictive plan and four gates (G1-G4) around four sprints; sprint reviews feed the gates | week 7 (G2 MVP checkpoint) | 1. Gates become paperwork and slow the team. 2. Two vocabularies confuse a first-time team | High (4.05): meets the week-3 and week-14 demands and keeps feedback every 2 weeks |

## Weighted score (from approach-scoring.csv)
Waterfall 2.60 · Scrum 3.70 · Hybrid 4.05

## Sensitivity
- Test 1: technical uncertainty (hardest to judge, because the proxy risk is unconfirmed) 20 -> 30, governance 20 -> 10. Scrum 4.00, Hybrid 3.95, Waterfall 2.20. The ranking changes: Scrum edges ahead by 0.05, so the hybrid's lead depends on the governance weight.
- Test 2: team experience 15 -> 25, early delivery 20 -> 10. Hybrid 3.95, Scrum 3.40, Waterfall 2.80. The ranking holds and the hybrid's lead grows.

## Recommendation
Hybrid (4.05), with Scrum as runner-up (3.70). Choose Scrum instead only if the sponsor drops the week-3 plan approval and attends every sprint review. Without that, the governance weight falls and Scrum overtakes, as test 1 shows.