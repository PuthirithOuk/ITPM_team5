# Weighted scoring: build, buy or hybrid · Realtime Quiz

## Weights (agreed 2026-10-06, before scoring)
| Criterion | Weight | Why |
|-----------|--------|-----|
| Learning value for the capstone | 40 | The project is a capstone: the course outcome (S10) is the reason the team exists, so it carries the largest weight. |
| Cost within the 200 USD cash budget | 25 | Cash is a fixed side (C-03) with no approver for overspend. |
| Time to the week-14 pilot | 20 | Time is the driver (C-01), but all three options can reach week 14, so it weighs less than cost. |
| Fit to the 47 functional requirements | 15 | Fit matters, but missing Should features is tolerable (scope flexes). |
| **Sum** | **100** | `=SUM(B2:B5)` = 100 |

## Options
- **Build**: the capstone as planned. Spring Boot backend on the Linode VPS (4 x 25 USD = 100 USD) plus domain (15 USD).
- **Buy**: a hosted quiz service. Named product: **Kahoot! 360 Pro Start**, listed at about 19 USD per month for up to 50 participants, billed yearly (228 USD/year). Sources give different prices (some list 3.99 to 9.99 USD per teacher on education plans); the 19 USD figure is the one repeated for the 50-participant tier. Check the vendor's page before relying on it.
- **Hybrid**: buy the live-session engine, build only authoring, analytics and export. No quiz vendor is known to expose a live engine as an embeddable API, so Hybrid is treated as a subscription plus a small VPS; scores for Hybrid are the least certain.

## Scores and evidence (1 = worst, 5 = best)
| Criterion | Build | Buy | Hybrid | Evidence |
|-----------|-------|-----|--------|----------|
| Learning | 5 | 1 | 3 | Build: the full stack is the learning outcome. Buy: 0 h of engineering. Hybrid: authoring, analytics and export only. |
| Cost | 4 | 2 | 2 | Build: 100 + 15 = 115 USD, 57.5 % of the cap, 85 USD kept for tools and reserve. Buy: 228 USD billed yearly = 114 % of the cap (even 4 x 19 = 76 USD would be paid on top of the unspent plan). Hybrid: VPS 100 + domain 15 + subscription 76 to 228 = 191 to 343 USD. |
| Time | 3 | 5 | 4 | Build: 504 h of work against 560 h of capacity, only 56 h of slack. Buy: running in days. Hybrid: engine bought, about 6 features still built. |
| Fit | 5 | 3 | 3 | Build: all 47 FR by definition. Buy: quizzes, timer and leaderboard exist, but no department-owned data, roles or CSV on the pilot plan. Hybrid: the engine's limits still apply. |

```
                       Weight  Build  Buy  Hybrid
Learning value           40      5     1     3
Cost within 200 USD      25      4     2     2
Time to week-14 pilot    20      3     5     4
Fit to requirements      15      5     3     3
Weighted score                 435   235   295
Percent of 500                 87 %  47 %  59 %
```
Hand calculation:
- Build = 40x5 + 25x4 + 20x3 + 15x5 = 200 + 100 + 60 + 75 = **435** (435 / 500 = 87 %)
- Buy = 40x1 + 25x2 + 20x5 + 15x3 = 40 + 50 + 100 + 45 = **235** (47 %)
- Hybrid = 40x3 + 25x2 + 20x4 + 15x3 = 120 + 50 + 80 + 45 = **295** (59 %)

Formulas (see `scoring.csv`; a live version is `scoring.xlsx`): `=SUM(B2:B5)`, `=SUMPRODUCT($B$2:$B$5,C2:C5)`, `=C7/(5*$B$6)`. The CSV has one SUMPRODUCT row per option (rows 7 to 9) and one percentage row per option (rows 10 to 12).

## Sensitivity
Move 10 points from the heaviest criterion (learning, 40 to 30) to the lightest (fit, 15 to 25).
- Build = 30x5 + 25x4 + 20x3 + 25x5 = 150 + 100 + 60 + 125 = **435**
- Buy = 30x1 + 25x2 + 20x5 + 25x3 = 30 + 50 + 100 + 75 = **255**
- Hybrid = 30x3 + 25x2 + 20x4 + 25x3 = 90 + 50 + 80 + 75 = **295**

The winner is unchanged: Build. Buy would need roughly a 180-point swing in its favour to win, so the result is robust. The weak point is not the weights but the Build time score: if the 504 h plan overruns by more than the 56 h contingency, time drops to 2 and Build falls to 415, still first.
