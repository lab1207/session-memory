# Install SMAA

One open format ([Agent Skills spec](https://agentskills.io)): the same `SKILL.md` works across 27+ agents. Link the clone where yours looks, then restart the agent session — `/skill` lists it.

## OpenCode (all projects)

```powershell
git clone https://github.com/lab1207/smaa ~/smaa
New-Item -ItemType Junction -Path ~/.config/opencode/skills/smaa -Target ~/smaa
```

## Claude Code, Cursor, compatible CLIs

```powershell
git clone https://github.com/lab1207/smaa ~/smaa
New-Item -ItemType Junction -Path ~/.claude/skills/smaa -Target ~/smaa
```

Same layout, zero extra setup.

## OpenAI Codex

```powershell
git clone https://github.com/lab1207/smaa ~/smaa
New-Item -ItemType Junction -Path ~/.codex/skills/smaa -Target ~/smaa
```

Project scope instead: link to `./.codex/skills/smaa` inside the project.

## Project-local (any harness)

Link into the project so the skill travels with it:

```powershell
New-Item -ItemType Junction -Path <project>/.opencode/skills/smaa -Target ~/smaa
```

## Others (Gemini CLI, Copilot, Windsurf, Amp, Roo, Goose, Cline, Continue…)

Same file — see your agent's skills docs or a registry like [skills.sh](https://skills.sh).

## Notes

- On macOS/Linux use `ln -s` instead of `New-Item`.
- Junctions mean `git pull` in the clone updates every consumer — no copies to drift.
- Fallback without installing: clone anywhere and point the AI at `AI_PROMPT.md`.
