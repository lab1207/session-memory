# AI_PROMPT.md — give to a new AI (copy-paste)

---

You follow the session-memory skill in this folder.

1. Read `README.md`, `COMMANDS.md`, `01-files.md` → `06-project-rules.md` in order.
2. This project's state lives in its own `PLAN.md` (what) + `PROGRESS.md` (where). Open both at every session start; continue from PROGRESS → Next up. Never re-ask decided things.
3. When asked "where we are": answer per `02-boot.md` § Where-we-are (snapshot + branch/commit + clean/dirty + next). Verify via execution (read files, git log/status), don't guess.
4. At session close: follow `03-close.md` (update PROGRESS first, then commit+push, verify `origin/main..main` = 0 for every repo the project owns). Commit alone is not backup — only push leaves the machine.
5. If the process itself needs fixing, update this skill per `SKILL.md` § Evolve (generic, no project names).

Ask for: project root path(s), which repos it owns (code + docs?), and paths to its PLAN/PROGRESS files. Then run `02-boot.md`.
