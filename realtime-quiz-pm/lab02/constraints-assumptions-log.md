# Constraints and assumptions log · Realtime Quiz · v0.2 · week 4

Review at every milestone. An overdue assumption is treated as an open issue and escalates to the sponsor within five working days.

## Constraints

| Id   | Type       | Statement (measurable)                                                                                      | Source / owner                                      | Validate by |
|------|------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------|
| C-01 | Constraint | Pilot session with exactly 50 enrolled students runs no later than the end of week 14 (2026-11-27).         | Charter §7 Constraints; objective O2               | Fixed       |
| C-02 | Constraint | Team capacity is 4 students × 10 h/week = 40 h/week; no paid staff or additional headcount is permitted.   | Charter §7 Resources; recap 2026-10-06             | Fixed       |
| C-03 | Constraint | Total cash outlay (VPS + domain + tools + reserve) must not exceed 200 USD; overspend requires written sponsor approval within 5 working days. | Charter §7 Budget                   | Fixed       |
| C-04 | Constraint | Broadcast latency must be ≤ 500 ms at the 95th percentile under 20 concurrent sessions, verified at the week-13 load test. | Charter O3; NFR table (NFR-P1)      | W13 gate    |
| C-05 | Constraint | Student names, scores and session data must be stored behind authenticated role-based access control; unauthenticated access to any student record is unlawful under the university data-protection policy (PDPA §26). | University data-protection policy; FR-A1..FR-A4 | W7 gate (MVP demo) |

## Assumptions

| Id   | Type       | Statement (measurable)                                                                                              | Owner          | Validate by | Risk id |
|------|------------|---------------------------------------------------------------------------------------------------------------------|----------------|-------------|---------|
| A-01 | Assumption | All pilot quizzes use text-only questions (no images, audio or video); confirmed in writing by at least 2 of 3 instructors before W6. | PM             | W6          | R-01    |
| A-02 | Assumption | The university VPS allows persistent WebSocket connections on port 443 (wss://) with no firewall block; verified by a 60-second echo test before W3. | Tech lead      | W3          | R-02    |
| A-03 | Assumption | All 50 pilot students hold active university SSO accounts and can authenticate against the system by W13; confirmed by IT helpdesk before W11. | PM / IT helpdesk | W11       | R-03    |
| A-04 | Assumption | Spring Boot 3.x and React 18 remain on their current stable LTS releases (no breaking API change) through W14; monitored via GitHub release RSS weekly. | Tech lead      | W14 (ongoing) | R-04 |
| A-05 | Assumption | A classroom with stable WiFi supporting ≥ 50 simultaneous browser sessions (≥ 10 Mbps aggregate) is booked and confirmed by IT facilities no later than W12. | PM             | W12         | R-05    |

---

> **Note on DR-01 impact:** Decision record DR-01 (approved 2026-10-24) added milestone "Open day demo" at W10 and introduced risk R-10 "demo on unfinished analytics". A-01 remains open; validate-by deadline unchanged.

