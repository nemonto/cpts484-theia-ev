# AI usage log — Justus Jones

---

## 2026-10-18 · Repo orientation and D-3 scope
Tool: Claude Code (Claude Opus 5.5)  
What I asked for: a read-through of the Preliminary Project Plan and the repo, then which work
products were mine (D-3 owner, D-5 secondary per plan §2.3) and how D-3 depends on the others.  
What came back: a summary of the project, the WRS (§2 Issues = D-2, §3 Improved Understanding =
D-3), and the dependencies D-2 → D-3 → D-4/D-1/D-5/D-6. Useful: the summary and dependencies.
Rejected: the first role list it gave, which came from the repo README rather than plan §2.3. I
supplied the §2.3 table to correct it.  
What I changed: confirmed roles against plan §2.3 myself.  
Verified against: Team_EV_Preliminary_Project_Plan.docx §2.3; `03-wrs/README.md`.  

---

## 2026-10-18 · WRS §3 draft (D-3)
Tool: Claude Code (Claude Opus 5.5)  
What I asked for: a fresh WRS §3 for D-3, built only from Austin's §2
(`WRS-Section2-Updated.md`), without using the D-3 version Zichuo submitted on my behalf. I
checked out the commit before it (fc0a30e) so that version wasn't in the working tree.  
What came back: one draft with Problems P1–P8, Goals G1–G8, domain (ID1–ID3), stakeholders,
world assumptions, objectives FO1–FO10/NFO1–NFO7, FR1–FR13, NFR1–NFR7, and three traceability
tables. It kept the IDs §2 already cites in its "Satisfied by" rows. Useful: the structure and
traceability. Problems found later (see next entry): one world assumption contradicted the
Masterlist, four Masterlist assumptions were missing, and there were no priorities or error
behavior.  
What I changed: renamed it to `WRS-Section3-Updated.md` and set Austin Aragon as co-author.  
Verified against: WRS §2 "Satisfied by" rows; plan §2.3.  

---

## 2026-10-18 · Checking §3 against course documents
Tool: Claude Code (Claude Opus 5.5)  
What I asked for: check the draft against the course documents from Canvas, one at a time, and
fix what didn't match.  
What came back:  
- World Assumptions Masterlist v1.0: the draft said users *use* a cane or dog; the Masterlist
  says they *might*. Fixed. Added the four missing assumptions (English, smartphone
  accessibility experience, emergency dial-out, room-to-room only) and a Source column marking
  each assumption as Masterlist or Added.  
- Requirements Review Checklist: added a priority for every requirement, error behavior for
  FR1/FR2/FR3/FR10, and removed a design detail (a specific gesture) from FR1.  
- Preliminary Definition v1.0: mapped every statement to §3 (new table §3.3.4). FR10 only texted
  the caretaker though the Definition says "calls and messages"; fixed.  
- Project Specification I v2.0 and the sample WRS: §3 covers everything §III.2.2 asks for. Added
  §3.3.5 mapping each FR to the prototype, as the sample does, and the facing direction to FR1 to
  match the prototype's "Where am I?".  

Rejected: a suggestion to add a diagram; neither the spec nor our plan requires one.  
What I changed: <add your own edits>. Screens 3 and 5 of the prototype are images, so I checked
the FR9, FR11 and FR12 rows against the slides myself: <confirm>.  
Verified against: Preliminary Definition v1.0; World Assumptions Masterlist v1.0; Requirements
Review Checklist; Project Specification I v2.0 §III.2.2; 484 - WRS.pdf (sample); Theia Prototype
Mock-Up.  

---

## 2026-10-18 · Repo housekeeping and recovery
Tool: Claude Code (Claude Opus 5.5)  
What I asked for: role fixes in the 03-wrs files to match plan §2.3, this log, git guidance, and
later a rebuild of my files after I accidentally deleted my local clone.  
What came back: edits to `03-wrs/README.md` and the §3 header. It also edited the other folders'
READMEs, which I hadn't asked for. Rejected: those extra edits, which I reverted. After the
deletion it rebuilt §3 and this log from our conversation in my fork; I re-checked IDs and
traceability in the rebuilt file.  
What I changed: kept only the 03-wrs changes. I did all git operations myself; the AI made
no commits.  
Verified against: plan §2.3.  
