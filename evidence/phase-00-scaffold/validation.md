# Phase 00 - Repo scaffold: validation

| Check | Command | Expected | Result |
|---|---|---|---|
| Raw evidence excluded from git | `git check-ignore -v evidence-raw/phase00_2026-10-06.txt` | Matched by `.gitignore` rule | PASS |
| Tracked files match planned structure | `git ls-files` | docs, incidents, scripts, README, LICENSE; nothing from evidence-raw/ | PASS |

```text
PS> git check-ignore -v evidence-raw/phase00_2026-10-06.txt
.gitignore:2:evidence-raw/      evidence-raw/phase00_2026-10-06.txt

PS> git ls-files
.gitignore
LICENSE
README.md
docs/architecture.md
docs/build-log.md
docs/decisions.md
docs/lessons-learned.md
incidents/.gitkeep
scripts/.gitkeep
```
