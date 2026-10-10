# Changelog

## Unreleased

- 02-boot: bounded reads (snapshot + newest row first, third doc needs a reason, whole history never).
- 01/03: conditional doc updates (PROGRESS + log always; others only when their subject changed).
- 03: verified gate at close (run locked gate, record command + PASS/FAIL).
- 06: named blockers (classify with blocker + remedy; blocked runs drop the retry offer).
- Full-project audit: 04-test-plan + templates/TEST-PLAN, 05-problems + templates/PROBLEMS, 06-project-rules (scope/failure/versioned-truth/licensing/data/UI/evidence) — generic for app or website.
- COMMANDS.md: only 2 commands (`stop` → close ritual, `where we are` → resume).
- CONTRIBUTING.md: guardrails (one job, non-goals, PR rules, review checklist) so contributions can't dilute the skill.
- LICENSE: MIT so anyone can use and contribute back.
