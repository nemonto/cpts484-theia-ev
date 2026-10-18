# CptS 484 — THEIA (Team EV)

Team repository for **CptS 484 — Software Requirements Engineering, Fall 2026**.

**Project:** THEIA — an indoor navigation assistant for blind and visually impaired users.
This is a *requirements engineering* project: the team's job is to analyze the informal
*THEIA Preliminary Definition*, identify what is incomplete, inconsistent, ambiguous,
redundant, or unsound in it, and produce defensible requirements models and specifications
with end-to-end traceability. We are not building the app.

---

## Team

| Member | GitHub | Owner of | Co-author of |
|---|---|---|---|
| Zichuo Wang | [@nemonto](https://github.com/nemonto) | D-0, D-5, D-6 · Liaison | D-3, D-4 |
| James Zuniga | [@JZ-EECS](https://github.com/JZ-EECS) | D-1 | D-2 |
| Austin Aragon | [@Austin-AA](https://github.com/Austin-AA) | D-2 | D-1 |
| Justus Jones | [@Jorstors](https://github.com/Jorstors) | D-3 | — |
| Young Kim | [@YoungCorKim](https://github.com/YoungCorKim) | D-4 | D-5, D-6 |

Everyone reviews every work product.

**Role changes in the final week (W5):** James Zuniga replaced Justus Jones as D-2 co-author,
Zichuo Wang replaced Young Kim as D-3 co-author, and Young Kim replaced James Zuniga as D-5
co-author. Justus Jones (D-3 owner) did not reply to the team during the final week, so Zichuo
Wang completed WRS §3 for the assembly on Sat, Oct 17. On Sun, Oct 18, Justus submitted an
independent WRS §3 draft and his AI usage log (PR #1):
[`WRS-Section3-Updated.md`](docs/phase1/03-wrs/WRS-Section3-Updated.md),
[`AI_Usage_Log.md`](docs/phase1/05-ai-usage-teamwork/Jones_Justus_AI_Usage_Report/AI_Usage_Log.md).
After review against the slides and the prototype, its additions (priorities, acceptance
criteria, error handling, Preliminary Definition coverage) were merged into WRS v1.1. See the
final plan, §2.3.

## Links

- **Discord:** `https://discord.gg/9B6YkcuVz`
- **Project Plan (final Phase I, v1.2):** [`docs/phase1/01-project-plan/`](docs/phase1/01-project-plan/Team_EV_Project_Plan_Phase1_Final.docx)
- **Presentation video:** https://youtu.be/0aHIRkDOK3E

---

## Phase I submission (Sun, Oct 18, 2026)

**Everything submitted for Phase I is in [`Phase I/`](Phase%20I/)** (see its README for the file index).

| # | Deliverable | File in `Phase I/` |
|---|---|---|
| 1 | WRS document, v1.1 (§2 Issues, §3 Improved Understanding + traceability) | `Team_EV_WRS_Phase1.docx` / `.pdf` |
| 2 | Prototype mock-up + preliminary user manual | `Theia Prototype Mock-Up.pptx` / `.pdf`, `Theia-Preliminary User Manual v1.1.docx` / `.pdf` |
| 3 | Revised Phase I project plan (v1.2) | `Team_EV_Project_Plan_Phase1_Final.docx` / `.pdf` |
| 4 | AS-IS/TO-BE slides + [video](https://youtu.be/0aHIRkDOK3E) | `Theia-AS-IS_and_TO-BE_v2.1 Final.pptx` / `.pdf` |
| 5 | AI Usage and Teamwork Report | `Team_EV_AI_Usage_and_Teamwork_Report.docx` / `.pdf` |

The Peer Review form (D-7) is submitted by each member individually and is not in the repo.

---

## Phase I schedule

Every week ends with a **team review at the Sunday checkpoint**: everyone reviews that week's
output against the Requirements Review Checklist before the next week builds on it.

| Week | Dates | Work | Checkpoint / milestone |
|---|---|---|---|
| W1 | Sep 14–20 | Team set up; preliminary plan | **Preliminary Plan submitted — Sun, Sep 20** (not graded) |
| W2 | Sep 21–27 | Everyone reads the Preliminary Definition + Masterlist and logs ≥3 issues; issues list consolidated; the team's three scenario pairs chosen (plus the template's Stevie pair) | Sun, Sep 27: issues list + scenarios reviewed |
| W3 | Sep 28–Oct 4 | WRS §2 completed; WRS §3 Problems and Goals started; slide skeleton; prototype sketched; Top Priority scenario chosen | Sun, Oct 4: WRS §2 complete, Problems and Goals drafted |
| W4–W5 | Oct 5–18 | WRS §3 + traceability; slides; Top Priority scenario analysis; user manual. Midterm week, so this runs through W5 | Sun, Oct 11: midterm-week checkpoint |
| W5 | Oct 13–18 | Presentation recorded; all other work products finished by Fri; Zichuo assembles everything on Sat (WRS document, final plan, AI report, consistency check); submission Sun | Fri, Oct 16: video uploaded, other work done · Sat, Oct 17: assembly · **Phase I submission — Sun, Oct 18** |
| — | Sun, Oct 18 | Peer Review form, individual (moved from Mon, Oct 12) | **Peer Review form submitted — Sun, Oct 18** (mandatory) |

---

## Work products and owners

**One owner, one co-author, four reviewers.** The owner leads the work product and pulls in the
team's input. The co-author writes an agreed part of it with the owner, and can take it over if
the owner falls behind. The other four members (including the co-author) review it every week,
not only before submission. See plan §2.3.

| ID | Work product | Weight | Owner | Co-author | Folder |
|---|---|---|---|---|---|
| D-0 | Preliminary Project Plan + repo link | not graded | Zichuo Wang | — | `01-project-plan/` |
| D-1 | AS-IS/TO-BE scenarios — slides + 10–15 min video | 20% | James Zuniga | Austin Aragon | `02-as-is-to-be/` |
| D-2 | WRS §2 — Issues in the Preliminary Definition | 25% | Austin Aragon | James Zuniga | `03-wrs/` |
| D-3 | WRS §3 — Improved Understanding + traceability | 25% | Justus Jones | Zichuo Wang | `03-wrs/` |
| D-4 | Prototype mock-up + preliminary User Manual | 10% | Young Kim | Zichuo Wang | `04-prototype-user-manual/` |
| D-5 | Project Plan, final Phase I version | 10% | Zichuo Wang | Young Kim | `01-project-plan/` |
| D-6 | AI Usage and Teamwork Report | 10% | Zichuo Wang | Young Kim | `05-ai-usage-teamwork/` |
| D-7 | Peer Review form | mandatory | each member, individually | — | *not in repo — submit to instructor* |

**Shared by everyone:** at least three candidate issues from the Preliminary Definition during
the elicitation week (Sep 21–27). Roughly thirty minutes. This is what keeps D-2 from being one
person's opinion.

---

## Repository layout

```
README.md                          # this file — roster, liaison, links
Phase I/                           # final Phase I submission (graded files only)
docs/
  phase1/
    01-project-plan/               # D-0 / D-5, versioned
    02-as-is-to-be/                # D-1 slides (.pptx), video link
    03-wrs/                        # D-2 + D-3, traceability tables
    04-prototype-user-manual/      # D-4 mockups, user manual
    05-ai-usage-teamwork/          # D-6 per-member logs, screenshots, write-up
    reference/                     # pointers to course documents
```

---

## Working rules

These applied through Phase I and carry into Phase II.

1. **Log your AI usage as you go.** Keep evidence in `docs/phase1/05-ai-usage-teamwork/<Your_Name>_AI_Usage_Report/`
   (screenshots, or a short block per session using `log-template.md`). In Phase I most evidence
   was collected at the end and the record is thin in places; in Phase II, AI logs are part of
   each Sunday checkpoint.
2. **Save the outputs you rejected.** A hallucinated figure you caught, a requirement that
   contradicted the World Assumptions Masterlist, a traceability link that didn't hold — those
   are the strongest evidence D-6 can carry.
3. **No unreviewed AI output ships**. Nothing AI-assisted enters a
   deliverable until its owner has verified it against the source documents and one reviewer
   has checked it.
