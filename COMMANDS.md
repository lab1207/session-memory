# Commands (only 2 — this skill has no others)

## 1. `stop` — end today's session

> You say: **stop** (or `save everything` / `we stop here` / `end session` / `wrap up` — same ritual, aliases never new commands)

AI does (`03-close.md` in order, no skipping):

1. Updates `PROGRESS.md` first (snapshot date, Done/In-progress, fresh Next up, session-log row + evidence names).
2. Ticks pointed trackers (tests/UI/problems).
3. Commits + pushes EVERY owned repo (code + state). Commit alone is not backup.
4. Verifies `origin/main..main` = 0 in each repo, then replies: what shipped, Next up, push proof.

## 2. `where we are` — resume (tomorrow or anytime)

> You say: **where we are**

AI does (`02-boot.md` in order):

1. Reads PLAN → PROGRESS → pointed trackers; checks branch, last commits, `origin/main..main`, status per repo.
2. Replies short: location (path + branch + commit) → status (snapshot + 3–5 bullets) → Next up verbatim → clean/dirty per repo.
3. Continues from Next up. Never re-asks decided things.

## Lessons

1. **Close-intent synonyms.** Close intent arrives in many phrases; firing only on exact `stop` lets sessions end dirty. Cost: unclosed sessions, unpushed work. Rule: `save everything`, `we stop here`, `end session`, `wrap up` run the identical ritual � aliases, never new commands.
