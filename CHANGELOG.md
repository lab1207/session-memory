# Changelog

All notable changes are released with a version tag (`v1.0.0`, `v1.1.0`, …). Scheme: MAJOR = command or file-contract change (consumers must adapt), MINOR = new lesson/guide/template (drop-in), PATCH = wording/fix with no behavior change. Each release ships GitHub Release notes.

## Unreleased

(nothing yet)

## [2.0.0] - 2026-10-10

Renamed skill `session-memory` → `smaa` (ID, repo, display) — consumers referencing the old ID must adapt. Plus:

- README: rea-style centered header, collapsible FAQ, skill + docs badges, registration guide, Works-with matrix (27+ spec agents), SMAA display caps.
- Repo renamed twice with full reference updates; history scrubbed name-free earlier and kept clean.

## [1.1.0] - 2026-10-10

Five drop-in additions, fully backward compatible.

- Config for foreign layouts (01/02/03 + templates/CONFIG.md): optional SKILL-CONFIG.md overrides snapshot/history paths and gate command; missing = today's defaults. Push-rule/services deferred.
- 04: metered-resources rule (request only when queued, release when done — no setup specifics).
- 01/03: zip-if-changed with full procedure (baseline location, fingerprint command, zip destination, NO ZIP when identical).
- COMMANDS: close-intent synonyms (aliases run the identical ritual, never new commands).
- 04: gate discovery (detect locked gate once per stack, record it).

## [1.0.0] - 2026-10-10

First release: the whole skill as it stands.
- 02-boot: bounded reads (snapshot + newest row first, third doc needs a reason, whole history never).
- 01/03: conditional doc updates (PROGRESS + log always; others only when their subject changed).
- 03: verified gate at close (run locked gate, record command + PASS/FAIL).
- 06: named blockers (classify with blocker + remedy; blocked runs drop the retry offer).
- Full-project audit: 04-test-plan + templates/TEST-PLAN, 05-problems + templates/PROBLEMS, 06-project-rules (scope/failure/versioned-truth/licensing/data/UI/evidence) — generic for app or website.
- COMMANDS.md: only 2 commands (`stop` → close ritual, `where we are` → resume).
- CONTRIBUTING.md: guardrails (one job, non-goals, PR rules, review checklist) so contributions can't dilute the skill.
- LICENSE: MIT so anyone can use and contribute back.
