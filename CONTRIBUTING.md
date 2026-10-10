# Contributing to session-memory

> This skill has one job: **today stops clean, tomorrow asks "where we are" and continues — for any project.**
> Every contribution must serve that job. Anything else gets rejected, no matter how good it is alone.

## Non-goals (what this skill will never become)

- Not a task runner, not a project template gallery, not framework-specific (no Expo/Android/web-only content — that lives in sibling skills).
- Never more than the 2 commands (`stop`, `where we are`). New commands need a separate skill.
- No project stories, names, secrets, screenshots, or logs. Ever.

## What belongs / what doesn't

| Belongs | Doesn't belong |
|---|---|
| A sharper boot/close/answer step proven in a real project | Theory never tried on a real project |
| A generalized lesson (mechanism + rule, any project) | App/ROM/framework-specific detail |
| A missing template field with why | New template files for niche workflows |
| A fix to wording that confused a real user/AI | Rewrites for style alone |

## Rules per PR

1. **One lesson/fix per PR.** Small diffs get reviewed; big ones get closed.
2. **Lesson format (3 lines max)** in the right file (`01`–`06`, templates):
   `N. **Title.** What happened, generalized. Cost: what it wasted. Rule: the check preventing it.`
3. **Real-use bar:** new rule needs 2 sightings, or 1 sighting + maintainer repro. Flukes noted once, promoted on repeat.
4. **Generic or rejected:** no project/app/website names, no descriptions of what any project does, no device serials, numbers, tokens, screenshots, logs.
5. **`CHANGELOG.md` line** in the same PR under Unreleased.

## No names, ever (privacy rule)

Users' projects are mostly private — so this skill must never carry them:

- No app/website/project names in files, examples, commit messages, or PR titles/bodies. Write "a private project", "the app", "the site" — never the real name.
- No descriptions of what a project does ("a dialer that…", "a shop that…"). Mechanism + rule only.
- Same bar for maintainers: every commit message gets the no-names check before push. History is public forever — a name merged once leaks forever.
6. **Guides stay current:** if the lesson changes daily flow, update the guide it affects (lessons live in their file, rules live in their guide) — same PR.

## Review (maintainer merges when)

- [ ] Serves stop / where-we-are directly
- [ ] Generic (works for app AND website)
- [ ] Small, formatted, changelogged
- [ ] Nothing private leaked (project/app names, what-it-does descriptions, numbers, serials, tokens, images)

Rejected PRs get one line saying which check failed — contributors are welcome to re-cut and re-open.
