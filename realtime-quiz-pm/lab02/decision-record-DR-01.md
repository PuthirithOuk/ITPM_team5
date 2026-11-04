# DR-01 · Open-day demo scope, week 10

| Field | Value |
|-------|-------|
| **Status** | Approved |
| **Date approved** | 2026-10-24 |
| **Requested by** | Head of IT (sponsor) |
| **Recorded by** | PM |
| **Baseline updated by** | End of W5 (2026-10-31) |

---

## Context

At the end of W4 the sponsor requested that all five Should features (F09–F13, 110 h) be demonstrable at a departmental open day in **week 10**, while the week-14 pilot (C-01) remains unchanged.

**Fixed facts at the time of negotiation:**

| Constraint | Value |
|------------|-------|
| C-01 | Pilot with 50 students, week 14 (2026-11-27) — fixed |
| C-02 | Capacity 4 × 10 h/week = 40 h/week; no paid staff |
| C-03 | Cash budget ≤ 200 USD; 85 USD unallocated |

**Capacity analysis (W5–W10):**

- Available capacity W5–W10: 6 × 40 = **240 h**
- Must remaining (300 h planned − 148 h done): **152 h**
- Should total: F09 (20 h) + F10 (30 h) + F11 (24 h) + F12 (12 h) + F13 (24 h) = **110 h**
- Hours needed for all Should by W10: 152 + 110 = **262 h**
- Shortfall (contingency untouched): **22 h**; with 56 h contingency intact: **78 h ≈ 2 weeks**

"Everything by W10" is not supportable within C-02 and C-03.

---

## Options considered

| Option | Time | Cost | Quality |
|--------|------|------|---------|
| **1. Must + F09 (20 h) + F10 (30 h) by W10; F11/F12/F13 at W14** | 0 weeks slip; 38 h buffer | 0 USD extra | Full quiz functionality + responsive UI + live analytics at open day; export, notifications and multimedia at pilot |
| **2. Demo build with mocked analytics (8 h) at W10; full Should at W14** | 0 weeks slip; 80 h buffer | 0 USD extra | Live quiz session + static analytics preview at open day; all 110 h of Should scope intact for pilot |
| **3. All Should by W10 (original request)** | Requires consuming 78 h of contingency; 0 h buffer | 0 USD extra (or 936 USD TA — breaks C-03) | High risk: Must backlog jeopardised; zero buffer exposes W14 pilot to any single risk event |

---

## Decision

**Counter-proposal 1 approved.**

- F09 (Responsive Design, 20 h) and F10 (Analytics and Reporting, 30 h) move to the **W10 "Open day demo"** milestone.
- F11 (Export to CSV/PDF, 24 h), F12 (Real-time notifications, 12 h) and F13 (Multimedia in questions, 24 h) remain at the **W14 pilot** milestone.
- No Could features (F14–F17) start before W11.

---

## Consequences

1. **New milestone added:** "Open day demo" at W10 is now part of the schedule baseline.
2. **Scope reclassification for W10:** F09 and F10 are Must-deliver for the W10 milestone (they retain their Should class for the overall pilot).
3. **New risk logged:** R-10 "Demo on unfinished analytics" — F10 (Analytics, 30 h) is a complex feature; a partial implementation at W10 may show misleading data to the sponsor audience. Mitigation: freeze analytics to a read-only view by W9 and seed with realistic test data.
4. **Won't for W10:** F11, F12, F13, F14, F15, F16, F17 — none start before W11.
5. **Buffer at W10:** 240 − 152 − 20 − 30 = **38 h** (above the 10 % policy threshold of 24 h for a 240 h envelope).

---

## Approvers

| Name | Role | Signature / confirmation |
|------|------|--------------------------|
| Head of IT | Sponsor | Verbal approval 2026-10-24; email confirmation requested by 2026-10-26 |
| PM (lecturer) | PM | Recorded 2026-10-24; baseline update published W5 |

