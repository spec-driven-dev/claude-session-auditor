# security-audit

Claude Code plugin for auditing Claude Code sessions for security issues.

## Status

Skeleton only — the `audit-review` skill and hooks have no logic yet.

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
