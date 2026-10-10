---
name: ai-session-memory
description: Session memory skill for AI coding agents — stop and resume any project via stop / where-we-are commands, with PLAN (what) + PROGRESS (where) files. Use at session start, when asked where we are, and at session close.
---

# SKILL.md — ai-session-memory (living)

> Keeps any project resumable across days: today stops clean, tomorrow asks "where we are" and continues with zero re-asking.
> Distilled from a private project's `plan.md` + `PROGRESS.md` system. Generic — no names.

## How to use

1. New project → copy `templates/` (`PLAN.md`, `PROGRESS.md`), fill per `01-files.md`.
2. Session start → follow `02-boot.md` (read PLAN → PROGRESS → continue from Next up).
3. Asked "where we are" → answer per `02-boot.md` § Where-we-are (snapshot + git + next).
4. Session close → follow `03-close.md` (summarize → update PROGRESS → commit+push → verify 0 unpushed).
5. Learned something about the process itself → update this skill per § Evolve below.

## Evolve (2 min)

- Process fix (boot/close/answer format) → edit `01/02/03`, add `CHANGELOG.md` line.
- New template field → edit `templates/`, note why in changelog.
- Keep lessons generic (mechanism + rule, no project story). Project stories stay in that project's PROGRESS session log.
- Tag `v1`, `v2` per consuming project that proves it.
