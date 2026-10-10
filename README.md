# session-memory

> Today stops clean. Tomorrow asks "where we are" and continues. No re-asking decided things.

[![MIT license](https://img.shields.io/badge/license-MIT-4c4330?style=flat-square)](LICENSE) [![release](https://img.shields.io/github/v/release/lab1207/session-memory?style=flat-square)](https://github.com/lab1207/session-memory/releases) [![issues](https://img.shields.io/github/issues/lab1207/session-memory?style=flat-square)](https://github.com/lab1207/session-memory/issues)

**Two commands. Any project — app or website. Zero re-asking.**

[Commands](#commands-only-2) · [Quick start](#quick-start) · [How it works](#how-it-works) · [What's inside](#whats-inside) · [FAQ](#faq) · [Contributing](#contributing)

## Quick start

Give a new AI this repo and paste `AI_PROMPT.md`:

```
1. Clone session-memory next to your project.
2. Paste AI_PROMPT.md into a fresh AI session.
3. Say "where we are" to resume — or just start working, then say "stop".
```

The AI reads the guides, continues from `Next up`, and closes with everything pushed.

## Commands (only 2)

| You say | AI does |
|---|---|
| **`stop`** (or `save everything` / `we stop here` / `end session` / `wrap up`) | Close ritual (`03-close.md`): update PROGRESS → tick trackers → commit+push all repos → verify 0 unpushed → reply Next up |
| **`where we are`** | Resume (`02-boot.md`): read PLAN→PROGRESS, check git → reply location → status → Next up → clean/dirty, then continue |

Full detail: `COMMANDS.md`. Aliases run the identical ritual — never new commands.

## How it works

Two files, two jobs:

| File | Job | Changes |
|---|---|---|
| `PLAN.md` | WHAT we build (idea, scope, locked decisions) | Rarely |
| `PROGRESS.md` | WHERE we are (snapshot, Next up, session log) | Every session |

Optional per-topic trackers (tests, UI, backend, problem ledger) hold detail; PROGRESS holds pointer + verdict. Optional `SKILL-CONFIG.md` adapts foreign layouts (missing file = defaults). If PLAN and PROGRESS disagree, PROGRESS wins on status, PLAN wins on scope — and the conflict gets reported.

## What's inside

| File | Job |
|---|---|
| `SKILL.md` | Skill entry + evolve protocol |
| `COMMANDS.md` | The 2 commands in full |
| `AI_PROMPT.md` | Copy-paste prompt for a new AI |
| `01-files.md` | Which files exist, two-repo rule (code vs state) |
| `02-boot.md` | Session start + where-we-are answer format |
| `03-close.md` | Session close ritual |
| `04-test-plan.md` | How to write + run TEST-PLAN (any project) |
| `05-problems.md` | Problem ledger format + status words |
| `06-project-rules.md` | Scope, failure A/B/C/D + handoff, versioned truth, licensing, data/privacy, UI baseline, evidence |
| `templates/` | PLAN, PROGRESS, TEST-PLAN, PROBLEMS, CONFIG starters |
| `CONTRIBUTING.md` | Contribution guardrails (protects the skill's one job) |
| `CHANGELOG.md` | Version history (semver + release notes) |

## FAQ

**Does it work with my stack?**
Yes — app or website, any language. Project-specific bits (gate command, file paths) resolve per project; foreign layouts get `SKILL-CONFIG.md`.

**What if my project already has its own docs layout?**
Add `SKILL-CONFIG.md` with your snapshot/history paths — the skill reads it, no renaming needed.

**How do sessions stay resumable?**
Every `stop` ends with an updated snapshot, a fresh `Next up`, and everything pushed. Every `where we are` verifies by reading files + git, never by memory.

**Can I contribute?**
Yes — issues and PRs welcome. One lesson per PR, generic only, no project names ever. See `CONTRIBUTING.md`.

## Contributing

Issues and pull requests welcome — rules: `CONTRIBUTING.md` (one job, non-goals, one lesson per PR, real-use bar, generic-only, no names ever). Rejected PRs get the failed check named so they can be re-cut.

## License

[MIT](LICENSE) — use, modify, share freely.
