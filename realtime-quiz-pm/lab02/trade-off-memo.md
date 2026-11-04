# Trade-off memo · CR-03 · Pilot moves to week 12

**To:** Head of IT (sponsor) · **From:** PM · **Date:** 2026-10-13 · **Decision by:** end of W4 (2026-10-17)

## Fixed facts

- **C-01** Pilot with 50 students was week 14; dean's notice of 2026-10-10 moves the semester end to week 12 (2026-11-13).
- **C-02** Team capacity is 4 × 10 h/week = 40 h/week; 12 weeks give 480 h (was 560 h).
- **C-03** Cash budget is 200 USD; no paid staff or TA hours are available.

## Request

The dean's calendar change cuts capacity by 80 h (2 weeks × 40 h). Planned work is 504 h; available capacity is now 480 h. The 24 h shortfall must leave scope before any risk materialises; contingency falls from 56 h to 48 h (10 % of 480 h).

| Option | Time | Cost | Quality at the pilot |
|--------|------|------|----------------------|
| A Drop all Could features: F14 chat (40 h) + F16 question bank (30 h) + F15 anon join (12 h) + F17 admin (12 h) = 94 h cut | 0 weeks slip | 0 USD | Must 300 h and Should 86 h intact; no chat, shared bank or admin screen; 70 h buffer remains |
| B Pay a TA for the 72 h gap | 0 weeks slip | 72 × 12 = 864 USD | Exceeds cash cap 4× — **breaks C-03** |
| C Keep the pilot in week 14 | +2 weeks | 0 USD | Ignores the dean's binding notice — **breaks C-01** |

## Recommendation

**Option A.** It restores a 70 h buffer (10 h above the 48 h contingency) and touches no Must or Should feature. Option B exceeds the 200 USD cash cap by 664 USD with no approver. Option C contradicts the dean's calendar, which the team cannot override.

## If no decision by end of W4

The team continues building Must features only; Should work is deferred until W6 at the earliest. Every week of delay consumes 40 h of Must work and reduces the remaining buffer by 40 h. Waiting past W5 makes Should scope undeliverable even under Option A.

---

*Full analysis, including CR-01 (chat) and CR-02 (anon join), is in [change-requests.md](change-requests.md).*

