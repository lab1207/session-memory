<div align="center">

# SMAA: Session Memory for AI Agents

### Stop today, resume tomorrow — two commands, zero re-asking.

**Say "stop" to close clean. Say "where we are" to continue — on any project.**

[![MIT license](https://img.shields.io/badge/license-MIT-4c4330?style=flat-square)](LICENSE)
[![release](https://img.shields.io/github/v/release/lab1207/smaa?style=flat-square)](https://github.com/lab1207/smaa/releases)
[![issues](https://img.shields.io/github/issues/lab1207/smaa?style=flat-square)](https://github.com/lab1207/smaa/issues)

[Quick start](#quick-start) · [Commands](#commands-only-2) · [How it works](#how-it-works) · [FAQ](#faq) · [Contributing](#contributing)

<code>git clone https://github.com/lab1207/smaa</code>

<br />

</div>

---

## Quick start

Give a new AI this repo and paste `AI_PROMPT.md`:

```
1. Clone SMAA next to your project.
2. Paste AI_PROMPT.md into a fresh AI session.
3. Say "where we are" to resume — "stop" when done.
```

The AI reads the guides, continues from `Next up`, and closes with everything pushed.

## Commands (only 2)

| You say | AI does |
|---|---|
| **`stop`** (or `save everything` / `we stop here` / `end session` / `wrap up`) | Updates PROGRESS → pushes all repos → replies Next up |
| **`where we are`** | Reads PLAN→PROGRESS + git → replies status → continues from Next up |

Detail: `COMMANDS.md`. Aliases run the identical ritual — never new commands.

## How it works

| File | Job | Changes |
|---|---|---|
| `PLAN.md` | WHAT we build | Rarely |
| `PROGRESS.md` | WHERE we are (snapshot, Next up, log) | Every session |

Trackers hold detail, PROGRESS holds the verdict. Missing `SKILL-CONFIG.md` = defaults. Full map: `SKILL.md`.

## FAQ

<details>
<summary><strong>My stack?</strong></summary>

Any — app or website. Gate command and paths resolve per project.

</details>

<details>
<summary><strong>My own docs layout?</strong></summary>

Add `SKILL-CONFIG.md` with your paths, no renaming needed.

</details>

<details>
<summary><strong>Contribute?</strong></summary>

Issues and PRs welcome — one lesson per PR, generic only, no names ever. See `CONTRIBUTING.md`.

</details>

## License

[MIT](LICENSE)
