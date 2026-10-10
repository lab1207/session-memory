# 03 — Close (every session)

1. Update `PROGRESS.md` FIRST: new snapshot date, move finished → Done, set fresh Next up, append session-log row (date + what happened + evidence names), tick checklists.
2. Update pointed trackers (tests ticked, UI/backend/problems verdicts). One line per result with artifact names — "it failed" without evidence doesn't count. Run the project's locked gate and record command + PASS/FAIL.
3. Commit + push EVERY repo the project owns (code repo + state repo). A commit alone stays on one disk — only the push is backup. Code sessions push both; docs-only sessions still push state.
4. Verify close: in EACH repo `git log --oneline origin/main..main` prints **0**. If N > 0, push again.
5. Leave clean: evidence pruned (keep launch-proof/FAILs/final only), toggles/permissions restored, phone/state noted for next boot.

Never close with Next up = "continue". Name the exact file/row/command tomorrow starts at.

## Lessons

1. **Verified gate.** Ticking test boxes without running the canonical gate ships green-looking red. Cost: a close that certifies broken work. Rule: run the locked gate at close and record command + PASS/FAIL.
