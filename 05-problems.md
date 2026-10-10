# 05 — Problem Ledger (every bug found on real surfaces)

> One row per problem found while testing/using: status + fix + verify steps. Template: `templates/PROBLEMS.md`.
> Status words (fixed everywhere): open / fix-shipped-awaiting-verify / fixed-and-verified / not-started.

## Row format

```
## P1 — Short title — STATUS
- **Seen (date):** what happened, where, on what (device/browser/version). One sighting = fact; two = pattern.
- **Severity:** who it hurts + how often.
- **Fix (date):** what changed, file:line, why this approach. If unfixable via public API, document the dead end IN the code instead of silent workaround.
- **Verify:** exact steps + expected lines + visible change that prove it. Tick only on device/browser proof with evidence names.
```

## Rules

- Intermittent stays open with count (seen 1×, repro 0×) — never close on "seems gone".
- If fix didn't change symptom, row goes back to open (never reclassify silently).
- Silent no-ops (no error, nothing happened) always get a row: check system/activity logs for the real abort line, then fix mechanism, delete dead helper.
- ROM/browser-specific failures get device/version in the row; fix = supported API path + rollback/alert + both-ways proof.
