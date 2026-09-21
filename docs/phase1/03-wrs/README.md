# 03 — Worldly Requirements Specification (D-2 + D-3)

Two halves of a **single submitted WRS document**, listed separately because they are graded
separately and owned by different members.

| Part | Content | Owner | Co-author | Weight |
|---|---|---|---|---|
| D-2 | Section 2 — Issues in the Preliminary Definition | Austin Aragon | Justus Jones | 25% |
| D-3 | Section 3 — Improved Understanding (WRS model + traceability) | Justus Jones | Young Kim | 25% |

**Due:** Sun, Oct 18, 2026 · **Internal deadline for D-2: Sun, Oct 4, 2026**

## The dependency (DE-1 / risk R-2)

D-3 cannot be finished before D-2 stabilizes. That is why D-2 has an internal deadline two weeks
ahead of submission, and why the D-3 owner and co-author start on Problems and Goals in that same
week from the *draft* issues list rather than waiting for D-2 to be final. Justus co-authors D-2,
so the D-3 owner knows the issues from the inside.

The team reviews the WRS at every Sunday checkpoint: the issues list on Sep 27, WRS §2 and the
Problems/Goals draft on Oct 4, and §3 as it is drafted in W4–W5.

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
