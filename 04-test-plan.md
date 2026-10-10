# 04 — Test Plan (WHAT to test, per phase)

> The app-specific WHAT lives in the project's own `TEST-PLAN.md`. This file is HOW to write and run it — any project, app or website.
> Golden rule: never test on silent failure — a failed step stops the run, gets captured, classified.

## Writing rows

Each row = action + expected proof (log line AND visible change) + safety note if real-world side effects:

```
- [ ] **Row name:** do X → expect `log/line Y` + screen shows Z (screenshot/dump/selector).
      Safety: only test account/safe number/staging; screenshot proof before destructive tap.
```

- Group by phase/day in build order. Tick only on verified proof, never on "looks fine".
- Keep a **re-test section**: rows once trusted-but-unproven get one line each with exact proof needed. Start capture before the first action, not mid-test.
- After every run: tick boxes, note evidence names, move FAILs to the problem ledger (05).
- Name the locked gate once per stack (lockfile → package runner; `pyproject`/`requirements` → pytest; `go.mod` → go test; `Cargo.toml` → cargo test; else ask) and record it — "run the gate" is unactionable until the command is written down.

## Running (any surface)

1. Prep session (env up, tunnel/dev-server healthy, state clean) → begin top-to-bottom, in order. Metered resources (paid endpoints, metered devices, API credits): request only when the run is fully queued, release the moment live work ends — never hold them on standby.
2. Per step: act → capture (log tail + current screenshot/dump) → assert BOTH expected line AND visible change → record PASS/FAIL/HANDOFF in RESULT.md.
3. FAIL → failure protocol (06 § Failure): freeze + capture, classify A/B/C/D, never reclassify silently.
4. Close: RESULT complete (one line per step + artifacts), evidence pruned (keepers only), toggles/data restored, summary → PROGRESS.

## Lessons

1. **Gate discovery.** "Run the locked gate" is unactionable when nobody knows which command it is. Cost: skipped verification on new projects. Rule: detect once per stack, record it as the locked gate, never guess twice.
2. **Metered resources.** Holding paid endpoints, metered devices, or API credits on standby burns budget for zero work. Cost: meter running between sessions. Rule: request only when the run is fully queued; release the moment live work ends.
