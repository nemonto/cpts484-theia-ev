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
| Zichuo Wang | [@nemonto](https://github.com/nemonto) | D-0, D-5, D-6 · Liaison | D-4 |
| James Zuniga | [@JZ-EECS](https://github.com/JZ-EECS) | D-1 | D-5 |
| Austin Aragon | [@Austin-AA](https://github.com/Austin-AA) | D-2 | D-1 |
| Justus Jones | [@Jorstors](https://github.com/Jorstors) | D-3 | D-2 |
| Young Kim | [@YoungCorKim](https://github.com/YoungCorKim) | D-4 | D-3, D-6 |

Everyone reviews every work product.

**New teammates:** post your name + GitHub username in `#general` on Discord and you'll be
added as a collaborator with write access.

## Links

- **Discord:** `https://discord.gg/9B6YkcuVz`
- **Project Plan (v1.0 draft 3):** [`docs/phase1/01-project-plan/`](docs/phase1/01-project-plan/Team_EV_Preliminary_Project_Plan.docx)

---

## Phase I schedule

Every week ends with a **team review at the Sunday checkpoint**: everyone reviews that week's
output against the Requirements Review Checklist before the next week builds on it.

| Week | Dates | Work | Checkpoint / milestone |
|---|---|---|---|
| W1 | Sep 14–20 | Team set up; preliminary plan | **Preliminary Plan submitted — Sun, Sep 20** (not graded) |
| W2 | Sep 21–27 | Everyone reads the Preliminary Definition + Masterlist and logs ≥3 issues; issues list consolidated; three scenario pairs chosen | Sun, Sep 27: issues list + scenarios reviewed |
| W3 | Sep 28–Oct 4 | WRS §2 completed; WRS §3 Problems and Goals started; slide skeleton; prototype sketched; Top Priority scenario chosen | Sun, Oct 4: WRS §2 complete, Problems and Goals drafted |
| W4–W5 | Oct 5–18 | WRS §3 + traceability; slides; scenario analysis; FP + creeping rate; user manual. Midterm week, so this runs through W5 | Sun, Oct 11: midterm-week checkpoint |
| — | Mon, Oct 12 | Peer Review form, individual | **Peer Review form submitted — Mon, Oct 12** (mandatory) |
| W5 | Oct 13–18 | Presentation recorded; D-6 assembled; editing pass; plan finalized; submission | Fri, Oct 16: video uploaded · **Phase I submission — Sun, Oct 18** |

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
| D-2 | WRS §2 — Issues in the Preliminary Definition | 25% | Austin Aragon | Justus Jones | `03-wrs/` |
| D-3 | WRS §3 — Improved Understanding + traceability | 25% | Justus Jones | Young Kim | `03-wrs/` |
| D-4 | Prototype mock-up + preliminary User Manual | 10% | Young Kim | Zichuo Wang | `04-prototype-user-manual/` |
| D-5 | Project Plan, final Phase I version | 10% | Zichuo Wang | James Zuniga | `01-project-plan/` |
| D-6 | AI Usage and Teamwork Report | 10% | Zichuo Wang | Young Kim | `05-ai-usage-teamwork/` |
| D-7 | Peer Review form | mandatory | each member, individually | — | *not in repo — submit to instructor* |

**Shared by everyone:** at least three candidate issues from the Preliminary Definition during
the elicitation week (Sep 21–27). Roughly thirty minutes. This is what keeps D-2 from being one
person's opinion.

---

## Repository layout

```
README.md                          # this file — roster, liaison, links
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

1. **Log your AI usage from Sep 21.** Keep `docs/phase1/05-ai-usage-teamwork/log-<yourname>.md`
   and append a short block per working session — see the template in that folder. Two minutes
   per session. Reconstructing this in October produces a visibly thin record, and D-6 is
   graded on the evidence of review.
2. **Save the outputs you rejected.** A hallucinated figure you caught, a requirement that
   contradicted the World Assumptions Masterlist, a traceability link that didn't hold — those
   are the strongest evidence D-6 can carry. 
3. **No unreviewed AI output ships**. Nothing AI-assisted enters a
   deliverable until its owner has verified it against the source documents and one reviewer
   has checked it.
