# 06 — Project Rules (any build: app or website)

## Scope discipline

- Freeze new builds until current scope is verified on real surfaces; decisions after evidence, not before.
- ONE unit at a time: view/spec → code → typecheck → verify → log. Batch only trivial proven siblings.
- Per-topic trackers created when the topic first matters, not upfront. Read every capture immediately; fail fast.

## Failure protocol (A/B/C/D)

1. FREEZE & CAPTURE (log tail, screenshot/dump, last 200 lines; video if visual/timing).
2. CLASSIFY: **A** app bug (fix code → rerun this step) · **B** environment (fix setup → rerun) · **C** needs human (Handoff Card, park step, continue rest) · **D** blocked (2 fails or input needed → record + report + move on). Name the blocker + the one remedy; a blocked run drops the retry offer — re-offering an identical doomed run looks frozen.

```
HANDOFF #<n> — <step> [needed for: ...]
DO:    <one physical/manual action, exact>
WATCH: <what should happen>
SAY:   what you saw — or nothing if logs already prove it
```

## Versioned truth (fast-moving frameworks lie)

- Read versioned docs matching the INSTALLED version (`.../versions/vX.Y.Z/`), never unversioned latest.
- On mismatch (types pass, runtime throws): read installed `.d.ts`/changelog for the new path. Verify system/native APIs against the SDK itself, never memory.
- Never hand-pin framework-lib versions; use the toolchain's installer + its `--check` before every native/prod build.

## Licensing & reference hygiene

- Day 0: fix scaffold LICENSE for proprietary work (`UNLICENSED`); deps stay permissive (MIT/Apache/BSD) — never GPL libs.
- Learn concepts only from reference repos; never copy code/structure/assets; never AI-launder (translate/rewrite = same derivative problem). Notes in own words, repo closed while coding, re-derive from official docs when unsure.
- Reference/study folders stay outside build + outside git history (gitignored). Attribution file only when the license requires it (e.g. Apache adaptation).

## Data & privacy (default: local-first)

- Read user data live from platform stores; never keep a shadow copy. v1 sends nothing off-device (no analytics/calls beyond dev server).
- Backend/accounts/sharing wait for an explicit phase + privacy pass. First off-device call needs a written exception note.
- Test data: only designated safe accounts/numbers/staging; destructive taps need pre-proof screenshot; never touch real user data; restore every toggle/permission after its assert.

## Frontend baseline (any UI)

- Tokens first (bg/surface/text/muted/border/accent/danger), applied everywhere — no hardcoded hexes in screens.
- No emoji as icons ever; use a verified icon set (names type-checked). Every tappable has an accessible label; audit until 0 unlabeled.
- Empty states everywhere (illustrated circle + title + hint, one grammar). Animations minimal (one-line transitions; defer perf-risky pulses).
- Safe-area/inset on every root (status bar / notch / nav); verify titles clear the bar on device, not in the editor.

## Evidence hygiene (any surface)

- Logs primary (full session capture from START), structure/dump per step, screenshots sparingly (launch-proof / FAIL / final, ≤5 keepers). Rolling `current.png` overwritten; FAIL copies saved first. Video only for motion, deleted after judging. RESULT.md + session log are the record; raw captures are disposable and gitignored.
- Never diagnose file/UI state from a single image read: cross-check bytes/hash + live structure; manifest/spec = intent source of truth.

## Lessons

1. **Named blockers.** An unclassified failure re-offers an identical doomed run, which looks frozen. Cost: retry loops that can never succeed. Rule: every failure gets a named blocker + one remedy; blocked runs print the remedy instead of a retry.
