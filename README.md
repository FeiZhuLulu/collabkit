# CollabKit

Multi-agent progress sync framework for Claude Code.

Let Claude Code, Codex, OpenCode, and OpenClaw coordinate on the same project by reading each other's progress logs.

## Install

```bash
# Download and install the skill (directory structure required)
mkdir -p ~/.claude/skills/collabkit
curl -fsSL https://raw.githubusercontent.com/FeiZhuLulu/collabkit/main/collabkit/SKILL.md -o ~/.claude/skills/collabkit/SKILL.md
```

Then say `/collabkit` in any project.

## Features

The skill provides three commands:

1. **Init** — Guided setup. Asks which agents you use, your environment, creates the right rule files and directories.
2. **Handoff** — Reviews your session, runs `git diff`, writes a detailed handoff report.
3. **Sync** — Scans all agents' latest progress and shows a summary table.

## How It Works

Two types of data:

- **Progress** — 5-line micro-logs agents write automatically when a phase completes. For daily sync.
- **Handoff** — Detailed session reports you trigger manually before switching agents. For deep transitions.

## Verified Agents

| Agent | Auto-reads rules | Status |
|-------|-----------------|--------|
| Claude Code | `CLAUDE.md` | ✅ Verified |
| Codex | `AGENTS.md` | ✅ Verified |
| OpenCode | `AGENTS.md` | ✅ Mostly works |
| OpenClaw | `AGENTS.md` | 🔧 Untested |

## License

MIT
