# CptS 484 — THEIA (Team EV)

Team repository for **CptS 484 — Software Requirements Engineering, Fall 2026**.

**Project:** THEIA — an indoor navigation assistant for blind and visually impaired users.
This is a *requirements engineering* project: the team's job is to analyze the informal
*THEIA Preliminary Definition*, identify what is incomplete, inconsistent, ambiguous,
redundant, or unsound in it, and produce defensible requirements models and specifications
with end-to-end traceability. We are not building the app.

---

## Team

| Member | GitHub | Role |
|---|---|---|
| Harvey Nemonto | [@nemonto](https://github.com/nemonto) | Liaison (instructor contact), repo owner |
| _TBD_ | _TBD_ | |
| _TBD_ | _TBD_ | |
| _TBD_ | _TBD_ | |
| _TBD_ | _TBD_ | |

**New teammates:** post your name + GitHub username in `#general` on Discord and you'll be
added as a collaborator with write access. Then add yourself to this table.

## Links

- **Discord:** `<INVITE LINK>`
- **Canvas course page:** `<CANVAS LINK>`
- **Draft Preliminary Project Plan:** [`docs/phase1/01-project-plan/`](docs/phase1/01-project-plan/)

---

## Phase I key dates

| Date | Milestone |
|---|---|
| Sun, Sep 20, 2026 | Preliminary Plan submission — **not graded**, feedback only |
| Sun, Oct 4, 2026 | *Internal:* WRS §2 complete; Problems and Goals drafted |
| Oct 9–11, 2026 | *Internal:* review window — every member reviews every work product |
| Sun, Oct 11, 2026 | *Internal:* all work products in complete draft |
| Mon, Oct 12, 2026 | **Peer Review form** — individual, mandatory (see below) |
| Fri, Oct 16, 2026 | *Internal:* freeze — no new writing, assembly only |
| Sun, Oct 18, 2026 | **Phase I final submission** |

### About the Oct 12 Peer Review

It is a **contribution evaluation**, not a document review. Each member fills out one form per
teammate *including themselves*, assigns each person a percentage of the overall project
contribution, and the five percentages must add up to 100%. It is submitted individually to the
instructor as a single file with your own name in the file name. Peer grading is mandatory and
your course grade stays "incomplete" until it arrives — put it in your calendar now.

This is stated in week 1, not week 4, because it is the reason the repo is organized the way it
is: one named owner per work product, and work committed here as it is drafted rather than
dumped at the end. That way nobody has to reconstruct or argue about who did what — the commit
history shows it. It cuts both ways, and that is the point.

---

## Work products and owners

Model: **one owner, four reviewers.** Each work product has a single accountable point person;
the other four review it during the Oct 9–11 window. Owners are a starting proposal from the
draft plan (§2.3) — say so in `#general` if you'd rather swap.

| ID | Work product | Weight | Owner | Folder |
|---|---|---|---|---|
| D-0 | Preliminary Project Plan + repo link | not graded | Member A | `01-project-plan/` |
| D-1 | AS-IS/TO-BE scenarios — slides + 10–15 min video | 20% | Member B | `02-as-is-to-be/` |
| D-2 | WRS §2 — Issues in the Preliminary Definition | 25% | Member C | `03-wrs/` |
| D-3 | WRS §3 — Improved Understanding + traceability | 25% | Member D | `03-wrs/` |
| D-4 | Prototype mock-up + preliminary User Manual | 10% | Member E | `04-prototype-user-manual/` |
| D-5 | Project Plan, final Phase I version | 10% | Member A | `01-project-plan/` |
| D-6 | AI Usage and Teamwork Report | 10% | Member A | `05-ai-usage-teamwork/` |
| D-7 | Peer Review form | mandatory | each member, individually | *not in repo — submit to instructor* |

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

1. **Commit as you draft, not when you finish.** Slippage should be visible in the history, not
   discovered at the deadline.
2. **Decisions get posted in `#announcements`.** No objection within 24h = agreed.
3. **Log your AI usage from Sep 21.** Keep `docs/phase1/05-ai-usage-teamwork/log-<yourname>.md`
   and append a short block per working session — see the template in that folder. Two minutes
   per session. Reconstructing this in October produces a visibly thin record, and D-6 is
   graded on the evidence of review.
4. **Save the outputs you *rejected*.** A hallucinated figure you caught, a requirement that
   contradicted the World Assumptions Masterlist, a traceability link that didn't hold — those
   are the strongest evidence D-6 can carry. Most teams keep only the good outputs, which is
   backwards.
5. **No unreviewed AI output ships** (SC-5 in the plan). Nothing AI-assisted enters a
   deliverable until its owner has verified it against the source documents and one reviewer
   has checked it.

---

## Note on course materials

This repository is **public**. Course PDFs distributed by the instructor (the Preliminary
Definition, the project specification, the FAQ) are not committed here — see
[`docs/phase1/reference/`](docs/phase1/reference/) for where to get them. If the team would
rather keep everything in one place, make the repo private first and add the instructor/TA as a
collaborator.
