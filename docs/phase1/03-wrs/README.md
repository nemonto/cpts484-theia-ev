# 03 — Worldly Requirements Specification (D-2 + D-3)

Two halves of a **single submitted WRS document**, listed separately because they are graded
separately and owned by different members.

| Part | Content | Owner | Co-author | Weight |
|---|---|---|---|---|
| D-2 | Section 2 — Issues in the Preliminary Definition | Austin Aragon | James Zuniga | 25% |
| D-3 | Section 3 — Improved Understanding (WRS model + traceability) | Justus Jones | Zichuo Wang | 25% |

**Due:** Sun, Oct 18, 2026 ·

In W5, James Zuniga replaced Justus Jones as the D-2 co-author and Zichuo Wang replaced Young Kim
as the D-3 co-author (plan §2.3). Justus did not reply to the team during the final week, so
Zichuo completed §3 for the assembly on Sat, Oct 17. On Sun, Oct 18, Justus submitted an
independent §3 draft, `WRS-Section3-Updated.md` (PR #1). After review against the slides and the
prototype, its additions were merged into WRS v1.1.

## Contents

- **`Team_EV_WRS_Phase1.docx`** — the submitted WRS document, v1.1: cover, revision history,
  process, §1 Introduction, §2 Issues (18), §3 WRS (P1–P8, G1–G9, IFO/INFO, FR1–FR13 and
  NFR1–NFR7 with priorities and NFR acceptance criteria), §4 Prototype and User Manual,
  §5 Traceability (including §5.4 Preliminary Definition coverage).
- `WRS-Section2-Updated.md` — Austin's §2 source (merged into the document with plain-language edits).
- `WRS-Section3-Updated.md` — Justus Jones's §3 draft (Oct 18), built from
  `WRS-Section2-Updated.md`. Merged into v1.1: priorities, NFR acceptance criteria, error
  handling (FS1.3–FS1.4, FS3.6, FS8.2–FS8.3, FS10.7), and the Definition coverage table (§5.4).
  Not merged: parts that conflicted with the recorded slides or the prototype (see the D-6
  report, §5 item 7).
- `Issues.md` — the consolidated W2 issues list.

## D-2 — Issues

Cover all three sections of the Preliminary Definition:

- 2.1 domain, stakeholders, objectives
- 2.2 functional requirements
- 2.3 non-functional requirements

Each issue needs a classification (incomplete / inconsistent / ambiguous / redundant / unsound)
**and the design rationale for how the team resolves it**. Generic rationale is the clearest
tell of unedited AI output; rationale grounded in our own assumptions is the least imitable part
of the document.

**Everyone contributes at least three candidate issues** during the elicitation week
(Sep 21–27). Keep the cut list — which candidates were rejected as trivial or duplicated, and on
what criterion. It is evidence of judgment for D-6.

## D-3 — Improved Understanding

Trace **Problems -> Goals -> Objectives -> Requirement Specifications**, for both functional and
non-functional requirements.

Traceability is success criterion SC-2: every Goal traces backward to a Problem and forward to
an Objective; every Requirement Specification traces to an Objective. Keep the traceability
tables in this folder as they are built, not at the end.

## Watch for

- **Scope creep (R-3).** The course FAQ warns against an "abundant laundry list" of
  requirements. Converge.
- Consistency with `../reference/` — the *World Assumptions Masterlist v1.0* and the
  *Requirements Review Checklist*.
