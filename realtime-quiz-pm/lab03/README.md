# Lab-03: Life cycle and methodology · Realtime Quiz

For the Realtime Quiz project, we selected a **Hybrid approach** combining predictive stage-gate governance with iterative Scrum sprint cycles (weighted score: 4.15 vs Scrum 3.45 and Waterfall 2.50). The predictive framing directly satisfies the sponsor’s non-negotiable governance requirements—specifically an approved scope baseline by week 3 (G1) and a fixed pilot demonstration in week 14 (G4)—while insulating the 4-student team against scope creep. Concurrently, 2-week agile sprints (Sprints 1–4, weeks 4–11) provide the fast feedback loops, continuous integration, and test-driven refactoring necessary to resolve high technical uncertainties surrounding real-time WebSocket broadcasting and Spring Security 7. See full architectural justification in [tailoring-decision-record.md](tailoring-decision-record.md).

The sponsor maintains strategic control through four sequential stage gates (G1 Plan Approval, G2 MVP Checkpoint, G3 Release Candidate, and G4 Pilot Acceptance), clear management-by-exception tolerance thresholds (time, hours, scope, quality, risk), and a weekly 1-page highlight report. Day-to-day delivery is shielded within timeboxed sprints where the student team autonomously manages the sprint backlog, with the PM intervening only if a tolerance breach triggers a formal exception report.

## Files

| File | What it contains (one line) |
|---|---|
| `lab03/project-profile.md` | Scored profile table classifying project characteristics into the hybrid band (score 3.1) based on charter evidence. |
| `lab03/approach-comparison.md` | Multi-dimensional comparison of Waterfall, Pure Scrum, and Hybrid across fit, governance, risks, and early demo weeks. |
| `lab03/approach-scoring.csv` | Weighted scoring model evaluating candidate approaches using Task 1 criteria weights (SUMPRODUCT formula). |
| `lab03/tailoring-decision-record.md` | ADR-style tailoring decision record (TDR-01) with context, options, decision, trade-offs, and tailoring table. |
| `lab03/life-cycle.mmd` | Mermaid Gantt diagram mapping the 14-week hybrid schedule, 4 sprints, hardening, and phase gates G1–G4. |
| `lab03/life-cycle.svg` | Vector graphic rendering of the 14-week hybrid life cycle Gantt chart. |
| `lab03/scrum-setup.md` | Scrum accountabilities table, sprint 1 event calendar, Definition of Ready, and CI-verifiable Definition of Done. |
| `lab03/sprint-1-backlog.csv` | Prioritized Sprint 1 backlog of 7 Must items totaling 30 story points with Gherkin acceptance criteria. |
| `lab03/governance.md` | Measurable G1–G4 stage gate checklists, stage-by-stage tolerances, reporting mechanisms, and formal closure criteria. |

## Inputs reused

| Input | Version / tag |
|---|---|
| `lab01/charter.md` | v1.1 (2026-10-13) |
| `lab01/stakeholders.md` | v1.0 (2026-09-29) |
| `lab02/moscow.md` | v1.0 (2026-10-20) |
| `lab02/constraints-assumptions-log.md` | v1.0 (2026-10-20) |

## Change log

| Date | Version | Change |
|---|---|---|
| 2026-11-09 | 0.1 | Lab-03 · life cycle selection, Scrum setup and governance added |