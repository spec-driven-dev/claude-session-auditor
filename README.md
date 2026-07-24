# security-audit

Claude Code plugin for auditing Claude Code sessions for security issues.

## Status

`hooks/` captures `PreToolUse`, `PostToolUse`, and `Notification` events to a global append-only JSONL audit log (see `hooks/scripts/log-event.js`). The `audit-review` skill is still a placeholder — no analysis logic yet.

By default the log is written to `${CLAUDE_PLUGIN_DATA}/audit.jsonl` (persists across plugin updates); override the location via the plugin's `log_path` config option (`/plugin configure security-audit@security-audit-plugin`).

## Install (local)

From this repo's parent directory, add it as a marketplace and install the plugin:

```
/plugin marketplace add /absolute/path/to/claude-session-auditor
/plugin install security-audit@security-audit-plugin
```

## Layout

- `.claude-plugin/plugin.json` — plugin manifest
- `.claude-plugin/marketplace.json` — self-hosted marketplace listing
- `skills/audit-review/` — audit review skill
- `agents/` — plugin agents
- `hooks/` — plugin hooks
