# Realtime Quiz platform · project management repository

A department-owned web platform where instructors write multiple-choice quizzes and run live, timed sessions. Students join with a 6-character code and get instant feedback, scores and a leaderboard. This repository holds the project management work products for the 14-week capstone (week 1 starts 2026-09-29), one folder per lab.

## Key facts
| Item | Value |
|------|-------|
| Sponsor | Head of the IT department |
| Project manager | Supervising lecturer (2 h/week) |
| Team | 4 students x 10 h/week = 40 h/week |
| Effort | 560 h capacity = 504 h planned work + 56 h (10 %) contingency |
| Cash cap | 200 USD (VPS 100, domain 15, tools and reserve 85) |
| Fixed dates | MVP demo in week 7 (2026-11-16); pilot with 50 students in week 14 |
| Scope | 17 features: 8 Must, 5 Should, 4 Could (re-rated for the pilot in `lab02/moscow.md`) |
| Quality floor | Broadcast <= 500 ms at p95, coverage >= 80 % with CI green, WCAG AA |

## Repository layout
```
realtime-quiz-pm/
├── README.md                          # this file
├── lab01/
│   ├── charter.md                     # project charter v1.1
│   └── stakeholders.md                # first stakeholder list
└── lab02/
    ├── features.csv                   # 17 features, hours (single source)
    ├── constraints.md                 # constraint classification, project shape
    ├── triangle.drawio / triangle.png # iron triangle
    ├── moscow.md                      # MoSCoW for the pilot
    ├── scoring.csv / scoring.md       # weighted build-vs-buy scoring
    ├── change-requests.md             # CR-01 to CR-03 trade-offs
    ├── constraints-assumptions-log.md # C-01..C-06, A-01..A-07
    ├── trade-off-memo.md              # one-page memo to the sponsor
    ├── negotiation-script.md          # challenge
    ├── decision-record-DR-01.md       # challenge
    └── README.md                      # files, inputs reused, change log
```
`lab02/scoring.xlsx` (live formulas) is an optional extra next to `scoring.csv`.

## Labs
| Lab | Topic | Status | Entry point |
|-----|-------|--------|-------------|
| Lab-01 | Charter and first stakeholder list | Charter v1.1 draft, awaiting sponsor signature | `lab01/charter.md` |
| Lab-02 | Constraint analysis and trade-off memo | Done, including the challenge; memo on CR-03 awaits sponsor decision | `lab02/README.md` |

## Decisions
| Id | Title | Status |
|----|-------|--------|
| DR-01 | Open-day demo scope, week 10 | Approved 2026-10-24 (`lab02/decision-record-DR-01.md`) |

## Working conventions
- One branch per lab (`lab-01`, `lab-02`), one commit per task, message `Lab-02 Task n: <topic>`.
- Merge request title: `Lab-02 – Ouk Puthirith`; the description names the change request the memo addresses and says whether the challenge is included.
- Numbers must match across files. Hours live in `lab02/features.csv`; change one only with a written reason in that file.
- Tools: Markdown editor, draw.io 24.x, LibreOffice Calc or Excel, Git.

## Self-check (Git Bash, from the repository root)
```bash
wc -l lab02/features.csv                                  # 18
grep -c "^| F[0-9][0-9]" lab02/moscow.md                  # 17
grep -c "SUMPRODUCT" lab02/scoring.csv                    # 3
grep -c "^\*\*Recommendation" lab02/change-requests.md    # 3
wc -w lab02/trade-off-memo.md                             # <= 400
grep -c "^| lab02/" lab02/README.md                       # >= 10
```