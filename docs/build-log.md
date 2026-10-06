\# Build Log



Chronological record of the lab build, one entry per phase. Each entry links to its validation evidence and commit.

Design rationale is recorded in \[decisions.md](decisions.md); unexpected findings in \[lessons-learned.md](lessons-learned.md).



\---



\## Phase 00 — Repository scaffold



\*\*Date:\*\* 2026-10-06 · \*\*Commit:\*\* `abe4bb0` · \*\*Evidence:\*\* \[phase-00-scaffold/validation.md](../evidence/phase-00-scaffold/validation.md)



\- Created the repository structure: `docs/`, `incidents/`, `evidence/`, `scripts/`.

\- Added `.gitignore` excluding raw evidence (`evidence-raw/`), OPNsense XML configuration exports and VMware VM artefacts.

\- Added a README skeleton with section headings only; content follows as evidence is collected.

\- Recorded \*\*D-001\*\*: host management access restricted to the MGMT segment (VMnet40) — see \[decisions.md](decisions.md).

\- Validated that raw evidence is excluded from Git and that tracked files match the planned structure.
