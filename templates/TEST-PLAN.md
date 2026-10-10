# Project — Test Plan (WHAT to test)

> Work top-to-bottom in order. Golden rule: never test on silent failure — failed step stops, gets captured, classified.

## 0. Prep (every session)

- [ ] Env healthy (dev server/tunnel/device), state clean, capture started BEFORE first action
- [ ] Expected proof known per row below (log line + visible change)

## Phase 1 — ...

- [ ] **Row:** do X → expect `Y` + screen shows Z. Safety: ...

## Re-tests (trusted-but-unproven rows)

- [ ] **T1:** ... → proof: ... + evidence: ...

## After every session

- [ ] Tick boxes, RESULT.md one line per step, FAILs → problem ledger, summary → PROGRESS.md
