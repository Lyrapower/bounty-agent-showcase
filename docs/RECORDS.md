# Records

## Target

```json
{
  "target_id": "…",
  "lane": "C1",
  "source": "bounty platform | grant | paid eval | direct",
  "repo": "owner/name",
  "issue": 0,
  "reward": {"amount": "…", "currency": "USD"},
  "found_at": "ISO-8601",
  "window_days": 90
}
```

## Intent (written before any work)

```json
{
  "intent_id": "…",
  "target_id": "…",
  "issue_body_sha256": "…",
  "policy": {
    "file": "CONTRIBUTING.md",
    "sha256": "…",
    "quote": "<exact sentence permitting AI-assisted contributions>",
    "verdict": "allow | deny | none"
  },
  "taken": {"assignee": null, "open_prs": 0}
}
```

## Submission (append-only ledger row)

```json
{
  "intent_id": "…",
  "tested_tree": "…",
  "submitted_tree": "…",
  "base_is_ancestor": true,
  "gate": "PASS | HOLD_NO_POLICY | DEAD_TAKEN | BLOCKED_*",
  "pr_url": "…",
  "ai_disclosure": true,
  "at": "ISO-8601"
}
```
