# Negotiation · sponsor asks for all Should features by week 10

## Data sheet (week 4)

| Measure                                   | Value                                      |
|-------------------------------------------|--------------------------------------------|
| Capacity W5–W10                           | 6 × 40 = **240 h**                         |
| Must remaining (300 h planned − 148 h done) | **152 h**                                |
| Should total (Task 2 rating)              | F09 20 h + F10 30 h + F11 24 h + F12 12 h + F13 24 h = **110 h** |
| Needed by W10 = Must remaining + Should   | 152 + 110 = **262 h**                      |
| Shortfall by W10 (no contingency used)    | 262 − 240 = **22 h** (with 0 h contingency and Could untouched) |
| Shortfall with contingency intact (56 h)  | 22 + 56 = **78 h ≈ 2 weeks**              |
| Velocity, sprints 1–2 (story points done) | 18, 21 → avg **19.5 pts/sprint**           |

"Everything by week 10" is not fundable: delivering all Should features by W10 leaves a 22 h gap if contingency is consumed, or a 78 h gap if contingency must stay intact (charter risk policy).

---

## Script

**Sponsor:** I need every Should feature demonstrable at the open day in week 10. It is mostly small stuff — responsive design, analytics, a few extras.

**PM:** I understand the value of the open day. The data says it is not small: the remaining Must work is 152 h and the five Should features add 110 h, for 262 h needed by W10. Our capacity from W5 to W10 is 240 h. That is a 22 h shortfall before we touch contingency, and the charter requires we keep 56 h of contingency intact, making the real gap 78 h — roughly two weeks of team capacity.

**Sponsor:** Surely the team can work a bit harder for six weeks? Just put in some extra hours.

**PM:** Our contract with the university caps the team at 10 h/week per student — that is the fixed 40 h/week in C-02. Even if everyone donated overtime, that is uncosted time we cannot put in the plan. The 240 h number is the absolute ceiling for W5–W10.

**Sponsor:** Other project teams manage to hit stretch goals. I am sure your team is motivated enough.

**PM:** Motivation is not the constraint — hours are. At our average velocity of 19.5 story points per sprint, we complete roughly 39 points per two-week sprint. Six weeks is three sprints, giving us about 117 points of delivery. The Must backlog alone needs roughly 152 h; there is no spare capacity for all five Should features on top.

**Sponsor:** It is a small change to the plan — just move the Should features forward. The pilot is still in week 14; nothing is lost.

**PM:** Moving all Should features forward is not a small change — it displaces 110 h, which is 46 % of our remaining capacity. If we pull all Should features into W10, we either miss the Must backlog (and risk the pilot) or we burn the contingency entirely, leaving zero buffer for any risk between now and W14. Risk R-01 alone (text-only assumption unconfirmed) could cost 24 h.

**Sponsor:** Can we decide later? Let's revisit in week 7 after the MVP demo.

**PM:** Deciding later costs us options, not buys them. Every week we delay this decision, 40 h of Must work is consumed. If we wait until W7, only three weeks remain before W10 — 120 h of capacity — which is not enough for 152 h of Must work, let alone any Should features. We need a decision this week to protect the W10 date.

**Sponsor:** What if we bring in a teaching assistant for a few weeks?

**PM:** A TA costs 12 USD/h. The 78 h gap would cost 936 USD. Our total cash budget is 200 USD with 85 USD unallocated. That is 11 times the available reserve and breaks C-03 — there is no approver for that overspend.

**Sponsor:** So you are telling me the open day gets nothing new?

**PM:** No — I am telling you "all Should by W10" is not supportable by the numbers. But I have two options that give the open day a strong demonstration within the 240 h envelope. Here they are:

**Counter-proposal 1:** Complete all Must features plus F09 Responsive Design (20 h) and F10 Analytics and Reporting (30 h) by W10. Total: 152 + 20 + 30 = 202 h, leaving a 38 h buffer. The open day shows a fully functional, responsive quiz platform with live analytics. F11 Export (24 h), F12 Notifications (12 h) and F13 Multimedia (24 h) remain at the W14 pilot — no Could work starts before W11.

**Counter-proposal 2:** Deliver a demo build at W10 with mocked analytics data (8 h of wiring, no live database queries). The full Should scope — all 110 h — stays at the W14 pilot as planned. Buffer remains 240 − 152 − 8 = 80 h, well above contingency. The open day shows a live quiz session with a static analytics slide; instructors understand it is a preview.

**Sponsor:** Option 1 sounds better for the audience. Let us go with that — responsive design and real analytics by week 10.

**PM:** Agreed. I will record this as Decision Record DR-01 today, 2026-10-24. The new scope baseline will be published to the team by the end of W5. To confirm: F09 and F10 move to the W10 "Open day demo" milestone; F11, F12 and F13 remain at the W14 pilot; no Could features start before W11. I will also log a new risk, R-10, for the dependency on analytics being stable enough to demonstrate at W10.

