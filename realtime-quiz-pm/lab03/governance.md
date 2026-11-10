# Governance · Realtime Quiz hybrid life cycle

## Stage gates
### G1 · Plan approved · end of week 3 (2026-10-19)
Project Charter approved by sponsor and PM with 560 h capacity and 200 USD budget baseline.(Accord to lab01/charter.md)
Scope baseline established with 8 Must features and WBS level 2. (evidence: lab02/moscow.md and the scope statement)
Milestone schedule baselined over 14 weeks with 4 phase gates.
Git repository initialized with automated CI pipeline executing clean build and tests.
Linode VPS provisioned and reachable with Docker and reverse proxy configured.

**Input:** charter, scope statement, WBS, milestone schedule, budget allocation in hours and cash.
**Decision maker:** Sponsor(Head of IT Department).
**Outcome:** continue / continue with changes / stop / repeats.
---

### G2 · MVP checkpoint · end of week 7 (2026-11-16)
Live end-to-end demo of all Must features working together in one session.
Live session successfully executed with instructor and simulated student joining via 6-character code.
Real-time WebSocket question broadcast and instant scoring functional.
Automated line coverage >= 80% on backend service code.
Cumulative effort within 280 person-hours spent.

**Input:** Sprint 2 review notes, working software demo, CI test and coverage report, timesheet summary.
**Decision maker:** Sponsor with the PM.
**Outcomes:** continue / continue with changes / stop / repeat.
---

### G3 · Release candidate · end of week 11 (2026-12-14)
All 8 Must features and at least 80% of Should features (F09, F10, F11, F12) meet Defintions of Done.
Automated line coverage >= 80% on core service and WenSocket handler modules..
Stress load test passed: 20 concurent sessions of 100 simulated participants on 2 vCPU and 2 GB RAM with 0 dropped session.
Real-time broadcast latency at 95th percentile (p95) < 500 ms under peak load.

**Input:** Spint 4 review notes, release candidate build artifact, load test report, security audit log, timesheet summary.
**Decision maker:** Sponsor with the PM.
**Outcomes:** continue / continue with changes / stop / repeat.
---

### G4 · Acceptaance and closure · week 14 (2027-01-04)
Pilot completed with 50 concurrent students in a live classroom quiz session with 0 blocking defects.
Instructors export of quiz grades to CSV verified and reconciled against manual tally.
Total student effort expended <= 560 hours and cash expenditure <= 200 USD.
Operational hand-over package delivered: source repository, VPS root credentials.
Project retrospective and lessons learned log documented and archived.

**Input:** Pilot session report, final budget reconsiliation, operations runbook, lesson learned document.
**Decision maker:** Sponser (Head of IT Department)
**Outcomes:** continue(accept and close) / continue with changes (conditional close) / stop / repeat.
---

## Tolerance (manage by exception)
| Tolerance | Stage 1 (W1-3) | Stage 2 (W4-7) | Stage 3 (W8-11) | Stage 4 (W12-14) |
| --- | --- | --- | --- | --- |
| Time | +3 days (G1 must hold) | +0 days (G2 fixed) | +3 days | +0 days (pilot date non-negotiable) |
| Cost (hours) | +10 % (max 132 h of 120 h) | +10 % (max 308 h of 280 h) | +5 % (max 462 h of 440 h) | 0 % (hard cap: 560 h total capacity) |
| Scope | 0 Must dropped; 0 WBS level 1 dropped | 0 Must dropped; Could features de-scoped | 0 Must dropped; Should features de-scoped to 50 % | 0 Must dropped; Should features frozen |
| Quality | CI green; 0 critical linter errors | Line coverage >= 75 %; 0 blocker bugs | Line coverage >= 80 %; p95 latency <= 600 ms | Line coverage >= 80 %; 0 blocker bugs; p95 <= 500 ms |
| Risk | Residual risk score < 15 | Residual risk score < 12 | Residual risk score < 10 | 0 unmitigated high risks |

**Escalation path:** Developers -> Scrum Master -> Project Manager -> Sponsor
**Exception report trigger:** An exception report is triggered immediately whenever a forecast shows that any stage tolerance (time > 0 days for fixed gates, cumulative hours > tolerance limit, any mUst feature at risk, or p95 latency > 500ms) will be breached before the next stage
---

## Reporting

### 1. Weekly highlight report
- **Frequency & Timing:** Submitted every friday by 17:00 by the PM to the sponsor.
- **Format & Length:** 1 page PDF or email summary.
- **Mandatory sections:**
    1. **Done:** Deliverables and backlog items completed during the current week.
    2. **Next:** Objectives, sprint events, and deliverables planned for next week.
    3. **Risk:** Top active risks, changes in severity, and status of mitigation actions.
    4. **Tolerance status:** RAG (Red/Amber/Green) dashboard for Time, Cost, Scope, Quality, and Risl against agreed stage tolerance.

### 2. Spint review chanckpoint
- Help every two weeks at the conclusions of each sprint (W5, W7, W9, W11)
- The PM uses this event as a formal monitoring checkpoint to inspect the working software increment, compare actual team velocity against the planned burn-up, and audit DoD compliance prior to the weekly highlight report.

### 3. Exception report template
When a tolerance threshold is threatened, the PM delivers a 3-part exception report within 24 hours:
    1. **Deviation:** Description of the variance, root cause, and impact on project baseline.
    2. **Options considered:** Analysis of viable alternative with associated trade-offs.
    3. **Recommendation:** Recommended course of action, required sponsor decision, and deadline for sponsor approval.
---

## Closure criteria
| Area                   | Criterion | Verified by | Owner |
|------------------------|-----------|-------------|-------|
| Acceptance             | Live pilot run in week 24 with 50 students; all 8 Must features verified with zero blockingdefectsl instructor sign-off on CSV export | Sponsor & instructor | Project Manager |
| Hand-over              | Git repository transferred to IT department namespace; Linode VPS admin credentials delivered via password manager; operations runbook accepted | IT Operations Lead | Student A (DevOps / SM) |
| Lessons learned        | 4 sprint retrospectives synthesized; final 2-hour project closure workshop held with the team and PM; lessons learned report archived | Project Manager | Student B (Product Owner) |
| Administrative closure | All timesheets approved (<= 560 h total); hosting expenses reconciled (<= 200 USD); domain DNS ownership transferred; project archive tagged v1.0-pilot | 	Department Finance & PM | Project Manager |