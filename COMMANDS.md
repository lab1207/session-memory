# Commands (only 2 — this skill has no others)

## 1. `stop` — end today's session

> You say: **stop**

Ambiguous bare `stop` (2 words or fewer, no object) may mean pause-output, not end-session — ask one confirming question first.

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

1. **Ambiguous stop.** A bare `stop` sometimes means pause-output, not end-session; the full close on it wastes pushes and surprises. Cost: backup ritual fired by accident. Rule: 2 words or fewer with no object → one confirming question before the ritual.
