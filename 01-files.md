# 01 — Files (one job each)

- `PLAN.md` — WHAT we build: idea, scope, phases, locked decisions, open questions. Rarely changes. New decisions append here once.
- `PROGRESS.md` — WHERE we are: status snapshot (date), Done / In progress / Pending, **Next up** (the handoff), session log table, reminders. Updated EVERY session, before anything closes.
- Optional per-topic trackers (create when topic first matters, not upfront): tests checklist, UI/design state, backend/data, problem ledger. Each owns its topic; PROGRESS points to them, never duplicates them.
- Doc index (optional, grows late): one-line map of every doc + reusable artifacts. Exists to make future distillation trivial.

Rules:

- One status home: PROGRESS snapshot. Trackers hold detail; PROGRESS holds pointer + verdict.
- Status words fixed: done / in-progress / pending / blocked. Same words everywhere.
- Dates on every snapshot and log row (`YYYY-MM-DD`). "Recent" without a date is forbidden.
- Update minimum: PROGRESS + session-log row every session; every other doc only when its subject changed (files added/moved, milestone moved, user-visible facts changed).

## Two repos (code vs state)

- Code repo (e.g. `MyApp/`): app source only. Its `.gitignore` excludes `testing/`, `metro.log`, build dirs. Raw evidence never committed.
- State repo (workspace root): PLAN + PROGRESS + trackers + problem ledger only. Its `.gitignore` excludes every app folder (each app is its own repo) + reference/study folders.
- Why separate: code history stays clean for builds; state history keeps full process record (decisions, test proof maps, lessons for future skills). Either can die without killing the other.
- Both private, both pushed every session. Commit alone stays on one disk — only the push is backup.

## Lessons

1. **Conditional updates.** Updating every doc every session rots docs with noise. Cost: stale words nobody trusts. Rule: PROGRESS + log always; others only when their subject changed.
