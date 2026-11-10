# Scrum setup · Realtime Quiz

Sources: [TDR-01](tailoring-decision-record.md), [MoSCoW list](../lab02/moscow-list.md), [charter](../lab01/project-charter.md)

## Roles
| Role            | Person       | Accountable for | Not responsible for |
|-----------------|--------------|-----------------|---------------------|
| Product owner   | Student A    | Product backlog content and order; acceptance of items; the link to the sponsor's needs | Technical design choices; running the events; budget and gates |
| Scrum master    | Student B    | Scrum events held and timeboxed; removing impediments; coaching the team on Scrum | Deciding priorities; writing most of the code is allowed but not required; project budget |
| Developers      | Students A-D | Sprint backlog, design, code, tests, and a done increment every sprint | Setting priorities alone; stakeholder or gate decisions |
| Project manager | Lecturer     | Gates, hours budget, tolerances, stakeholders, risks, escalation | Telling developers how to build; ordering the backlog; attending daily scrums |
| Sponsor         | Head of IT   | Approving the plan and gates, providing the pilot users and the final acceptance | Day-to-day decisions; backlog items; technical solutions |

Conflict: Student A is product owner and also a developer, so priorities could bend to what is easy to build. We limit this by asking the PM to check the backlog order at each sprint review and by making the Must list, baselined at G1, off limits for the PO alone.

## Sprint goal (sprint 1, weeks 4-5)
By 2 November, a lecturer or student can register, log in with a role and create a quiz, on a project that builds and tests automatically.

## Event calendar · sprint 1 (2026-10-20 to 2026-11-02)
| Event | Date(s) | Time | Timebox | Attendees | Output |
|-------|---------|------|---------|-----------|--------|
| Sprint planning | Tue 2026-10-20 | 10:00 | 2 h (max 4 h) | PO, SM, developers | sprint goal, sprint backlog |
| Daily scrum | Mon-Fri 2026-10-21 to 2026-11-02 (9 days) | 09:00 | 15 min | developers (+SM) | updated plan for the day |
| Backlog refinement | Wed 2026-10-28 | 16:00 | 1 h (max 10 % of capacity) | PO, developers | sprint 2 items meet the DoR |
| Sprint review | Mon 2026-11-02 | 14:00 | 1 h (max 2 h) | team, PM, sponsor | feedback, backlog update |
| Sprint retrospective | Mon 2026-11-02 | 15:30 | 45 min (max 1.5 h) | team (PM optional) | 2 improvement actions |

Planning on day 1 replaces that day's daily scrum.

## Definition of ready
An item may enter sprint planning only if:
1. It has an FR id from the MoSCoW list.
2. It has at least one acceptance criterion in Given/When/Then form.
3. It has a Fibonacci estimate (1, 2, 3, 5, 8) agreed by all developers; anything larger is split first.
4. Its dependencies are named and either done or in the same sprint.
5. It has a sketch, API outline or example of the expected behaviour (a screen or request/response is enough).

## Definition of done
1. Code is merged to main through a reviewed merge request (at least one other student).
2. The build (`mvnw verify`) passes in the CI pipeline. (CI)
3. All automated tests pass, with no skipped tests. (CI)
4. Line coverage of new service code is at least 80 % in the JaCoCo report. (CI)
5. No new critical or high findings in the static analysis or dependency check. (CI)
6. Acceptance criteria are demonstrated in the review, on a desktop and on a phone-sized viewport.
7. No secrets or credentials in the repository.
8. Database changes are delivered as migrations and run on a clean database.
9. Documentation touched by the change (README, API notes) is updated.

## Sprint 1 planning
Planning velocity: 30 points · capacity: 4 x 10 h x 2 weeks = 80 h
Committed: 30 points (see [sprint-1-backlog.csv](sprint-1-backlog.csv); total checked with =SUM(E2:E8))