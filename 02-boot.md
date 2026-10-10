# 02 — Boot + Where-we-are

## Boot (every session, in order)

0. Read `SKILL-CONFIG.md` if present; resolve snapshot path, history path, gate command (missing file = PROGRESS.md + discovered gate). All steps below use the resolved paths.
1. Read `PLAN.md` → read snapshot + newest history row only → read pointed trackers only (tests/UI/backend/problems as needed). Never re-read full history: a third doc needs a stated reason.
2. Check git: branch, last 3 commits, `origin/main..main` count, short status (per owned repo).
3. Continue from PROGRESS → **Next up**. Never re-ask decided things. If Next up is stale, say so and propose the correction.

## Where-we-are (when asked "where we are")

Verify by execution, then answer short:

1. Location: workspace path + branch + commit (one line).
2. Status: copy PROGRESS snapshot date + Done/In-progress in 3–5 bullets.
3. Next: the Next-up handoff verbatim (1–3 lines).
4. Clean/dirty: `origin/main..main` = N per repo + untracked notable files.

Format: location → status → next → git. Facts only, no praise. Reference files as `path:line` when citing.

## Lessons

1. **Bounded reads.** A boot that re-reads full history plus every tracker burns context and re-surfaces decided things. Cost: slow boots, re-asked questions. Rule: snapshot + newest log row first, third doc only with a stated reason, whole history never.
