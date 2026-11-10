# Project profile · Realtime Quiz

Sources: [charter](../lab01/charter.md), [stakeholder list](../lab01/stakeholders.md), [MoSCoW list](../lab02/moscow.md), [constraint analysis](../lab02/constraints.md), Lab-03 handout recap table

| # | Criterion                            | Evidence (one fact)                                                                                           | Weight | Score 1-5 | W x S   |
|---|--------------------------------------|---------------------------------------------------------------------------------------------------------------|-------:|----------:|--------:|
| 1 | Requirements stability               | 8 Must features are fixed in the charter, but screens and real-time behaviour are not specified (MoSCoW list) |     25 |         3 |      75 |
| 2 | Technical uncertainty                | The campus proxy may block WebSocket, Spring Boot 4 examples are outdated, and late answers can cause race conditions (known risks) |     20 |         4 |      80 |
| 3 | Team experience with agile           | First Scrum project; Java and Spring are being learned in the parallel Software Engineering course (recap)    |     15 |         2 |      30 |
| 4 | Contract and governance constraints  | Sponsor requires an approved plan by week 3 and a pilot with 50 students in week 14; internal project, no contract (charter) |     20 |         2 |      40 |
| 5 | Need for early delivery and feedback | The pilot is a hard date in week 14, and the real-time UX can only be validated by playing a working quiz (charter, MoSCoW list) |     20 |         4 |      80 |
|   | **Profile** = SUM(W x S) / 100       |                                                                                                               |    100 |           | **3.05** |
| 6 | (optional) Sponsor availability      | Assumption: the Head of IT can review an increment every two weeks; not confirmed in the charter             |      - |         3 |       - |

Score 1-5: 1 = the fact favours predictive, 5 = it favours adaptive.

Interpretation: < 2.5 predictive · 2.5-3.5 hybrid · > 3.5 agile

Calculation: 75 + 80 + 30 + 40 + 80 = 305; 305 / 100 = 3.05, which falls in the **hybrid** band.

## Profile summary
Realtime Quiz is a fixed-date, fixed-scope-core project with real technical unknowns, run by a team that has never done Scrum and answers to a sponsor who wants an approved plan early. The two criteria that pull hardest towards an adaptive approach are technical uncertainty and the need for early feedback (both 80 points), while governance constraints and low agile experience pull towards a predictive one. Task 2 must therefore compare waterfall, pure Scrum and a hybrid of a predictive plan with gates around agile sprints.