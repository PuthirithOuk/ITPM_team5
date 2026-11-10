# TDR-01 · Life cycle and methodology for the Realtime Quiz project
Status: proposed · 2026-10-13 · to be decided by the sponsor (Head of IT) and the PM (supervising lecturer)

Sources: [project profile](project-profile.md), [approach comparison](approach-comparison.md), [scoring sheet](approach-scoring.csv), [charter](../lab01/project-charter.md)

## Context
Four students with about 10 h/week each (560 h in total) have 14 weeks, starting 2026-09-29, to deliver a realtime quiz platform. The sponsor, the Head of IT, requires an approved plan by the end of week 3 and a pilot with 50 students in week 14. The Must list (8 features) is fixed, but screens and real-time behaviour are not specified. Technical uncertainty is high: the campus proxy may block WebSocket, Spring Boot 4 examples are outdated, and late answers can cause race conditions. The team has never run a Scrum project and is learning Java and Spring in parallel. The project profile scores 3.05, which is in the hybrid band.

## Options considered
1. Waterfall (score 2.60): a full plan and a single acceptance; the first playable quiz appears around week 12, too late to find proxy or UX problems.
2. Pure Scrum (score 3.70): fast feedback every 2 weeks, but no baseline and no gate; the week-3 plan and the week-14 pilot date are not protected.
3. Hybrid (score 4.05): a predictive plan and four gates (G1-G4) around four two-week sprints, with sprint reviews feeding the gates.

## Decision
Adopt the hybrid life cycle (4.05, ahead of Scrum at 3.70 and Waterfall at 2.60). The two strongest reasons are that G1 and G4 map directly onto the sponsor's demands (plan by week 3, pilot in week 14), and that four sprints give the sponsor a working increment every two weeks, which is how the technical risks are found early.

## Consequences
+ The sponsor gets an approved plan in week 3 and four decision points with measurable evidence.
+ Technical risks (WebSocket, race conditions) surface in sprint reviews, not in week 12.
+ A first-time Scrum team has external structure (gates, lecturer as PM) while it learns the events.
- Gates can become paperwork and slow the team -> mitigation: each gate has at most five checklist items, and the evidence comes from the CI pipeline and the backlog export.
- Two vocabularies (WBS and sprint backlog) may confuse the team -> mitigation: the WBS is kept to level 2 and linked to backlog items by FR ids; the scrum master explains the mapping in sprint 1 planning.
- The scope baseline at G1 may clash with changing priorities -> mitigation: the Must list is baselined, order and detail inside it are free, and Should/Could changes go through the product owner and the PM.
- The tolerance rules add reporting effort -> mitigation: one highlight report per week, at most one page.

## Tailoring
| Keep from predictive | Keep from agile | Drop |
|----------------------|-----------------|------|
| WBS to level 2 (needed for the Lab-04 scope baseline) | Two-week sprints with review and retrospective (feedback and learning for a first-time team) | Full upfront design and detailed schedule beyond sprint 1 (requirements and technology are too uncertain) |
| Four phase gates with sponsor decisions (protect the week-3 and week-14 demands) | Prioritised product backlog with story points (fits the Must/Should/Could list) | Formal change-control board (a product owner and PM decision is enough for a four-person team) |
| Tolerances and weekly highlight report (the PM manages by exception) | Definition of done checked by CI (quality without a separate test phase) | Separate test phase before release (testing happens in every sprint; only hardening remains) |
| Budget tracked in hours against 560 h (the only real budget for the team) | Daily scrum, 15 min (keeps a small team aligned) | Sprint-by-sprint estimation of cost in money (the cash budget is a fixed VPS and domain) |

## Phase gates
| Gate | Week / date | Evidence required | Decision maker | Outcomes |
|------|-------------|-------------------|----------------|----------|
| G1 plan approved | W3 / 2026-10-19 | Scope statement and WBS to level 2 committed; schedule with the four sprints and hours budget of 560 h; risk register with at least 8 risks | Sponsor | continue / continue with changes / stop / repeat |
| G2 MVP checkpoint | W7 / 2026-11-16 | All Must items of sprints 1-2 meet the DoD (backlog export); line coverage ≥ 80 % in the JaCoCo report; hours used ≤ 55 % of 560 h | Sponsor with the PM | continue / continue with changes / stop / repeat |
| G3 release candidate | W11 / 2026-12-14 | All Must and at least 80 % of Should items meet the DoD; load test with 100 simulated students, p95 broadcast < 500 ms; hours used ≤ 90 % of 560 h | Sponsor with the PM | continue / continue with changes / stop / repeat |
| G4 acceptance and closure | W14 / 2027-01-04 | Pilot with 50 students completed and survey results collected; acceptance signed by the sponsor; runbook and repository handed over | Sponsor | continue (close) / continue with changes (extend) / stop / repeat (second pilot) |