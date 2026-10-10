# session-memory — resumable work across days

> Today stops clean. Tomorrow asks "where we are" and continues. No re-asking decided things.

## Commands (only 2)

| You say | AI does |
|---|---|
| **`stop`** | Close ritual (`03-close.md`): update PROGRESS → tick trackers → commit+push all repos → verify 0 unpushed → reply Next up |
| **`where we are`** | Resume (`02-boot.md`): read PLAN→PROGRESS, check git → reply location → status → Next up → clean/dirty, then continue |

Full detail: `COMMANDS.md`. Give a new AI `AI_PROMPT.md` first.

## Contributing (public repo)

Issues and pull requests welcome — rules: `CONTRIBUTING.md` (one job, non-goals, one lesson per PR, real-use bar, generic-only). Rejected PRs get the failed check named so they can be re-cut.

## Files

| File | Job |
|---|---|
| `SKILL.md` | Skill entry + evolve protocol |
| `COMMANDS.md` | Only 2 commands: `stop` + `where we are` |
| `AI_PROMPT.md` | Copy-paste to a new AI |
| `01-files.md` | Which files exist and their one job each |
| `02-boot.md` | Session start + "where we are" answer format |
| `03-close.md` | Session close ritual |
| `04-test-plan.md` | How to write + run TEST-PLAN (any project) |
| `05-problems.md` | Problem ledger format + status words |
| `06-project-rules.md` | Scope, failure A/B/C/D + handoff, versioned truth, licensing, data/privacy, UI baseline, evidence |
| `templates/PLAN.md` | Template: WHAT we build (rarely changes) |
| `templates/PROGRESS.md` | Template: WHERE we are (updated every session) |
| `templates/TEST-PLAN.md` | Template: WHAT to test |
| `templates/PROBLEMS.md` | Template: problem ledger |
| `CHANGELOG.md` | Version history |
| `CONTRIBUTING.md` | Contribution guardrails (protects the skill's one job) |
| `LICENSE` | MIT — use, modify, share freely |

## Rule

Two files, two jobs: PLAN = what (stable). PROGRESS = where (every session). If they disagree, PROGRESS wins on status, PLAN wins on scope — and report the conflict.
