Constraints and assumptions log · Realtime Quiz · v0.1 · week 2
Id	Type	Statement (measurable)	Source / owner	Validate by
C-01	Constraint	The pilot with 50 students runs in one session in week 14 (week 12 if CR-03 is approved).	charter section 4 and 7; sponsor	fixed
C-02	Constraint	Effort capacity is 4 students x 10 h/week = 40 h/week: 560 h in 14 weeks (504 h planned + 56 h contingency).	Lab-02 recap, Resources; charter section 5 (says 8 h/week, see README)	fixed
C-03	Constraint	Cash is capped at 200 USD: VPS 100, domain 15, tools and reserve 85; no paid staff.	charter section 7; sponsor	fixed
C-04	Constraint	One server instance of 2 vCPU and 2 GB RAM carries 20 concurrent sessions of 100 simulated participants; no secrets in the repository.	charter section 7 and O4	fixed
C-05	Constraint	Student names and results may be stored only after the data protection officer or registrar approves, by the week-13 gate.	stakeholder S11 (data protection officer or registrar)	fixed
C-06	Constraint	The MVP demo shows 8 of 8 Must features in week 7.	charter section 7 and O1; sponsor	fixed
A-01	Assumption	Each student logs at least 36 h of the 40 h/week (90 %) in every week from week 3 to week 14.	owner: PM	W3 -> R-01
A-02	Assumption	The Linode VPS at gicitc.com is reachable by the team by week 4 at a price of 25 USD/month or less.	owner: QA/DevOps student (S05)	W4 -> R-02
A-03	Assumption	50 pilot students and one instructor are booked for a single session, with the date fixed in writing by week 8.	owner: lecturers (S07), confirmed by sponsor	W8 -> R-03
A-04	Assumption	The one-page data description reaches the registrar by week 10 and the approval arrives by week 13.	owner: PM	W10 -> R-04
A-05	Assumption	The campus proxy passes WebSocket or the SockJS fallback in a test session before week 8.	owner: QA/DevOps student with network administrator (S09)	W8 -> R-05
A-06	Assumption	Feature estimates in features.csv are correct within +/- 56 h in total (11 % of 504 h) at the week-7 MVP.	owner: backend students (S03)	W7 -> R-06
A-07	Assumption	Pilot quizzes contain text only; two instructors confirm in writing that no question needs an image by week 6.	owner: lecturers (S07)	W6 -> R-07
Review at every milestone. Overdue assumption = open issue.
Risk ids R-01 to R-07 are placeholders until the Lab-03 risk register exists.