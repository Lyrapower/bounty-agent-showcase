# Submission gate

| Outcome | Code | Trigger |
|---|---|---|
| Submit | `PASS` | All checks below hold |
| Hold | `HOLD_NO_POLICY` | Repository has no written policy on AI / automated contributions |
| Dead | `DEAD_TAKEN` | Issue assigned, or another open PR exists |
| Blocked | `BLOCKED_TREE_MISMATCH` | Tested tree hash ≠ submitted tree hash |
| Blocked | `BLOCKED_BASE` | Base branch is not an ancestor of the submission |
| Blocked | `BLOCKED_POLICY_DENY` | Written policy forbids AI contributions |
| Skip | `DUP_INTENT` | An intent for this target already exists |

Notes

- A `HOLD` is not a failure. It is released only by a human decision and is never auto-released.
- Dead targets are kept as regression fixtures, so the gate is re-tested on real cases where it must refuse.
- The submission ledger is append-only. A correction is a new row, and no row is ever edited.
