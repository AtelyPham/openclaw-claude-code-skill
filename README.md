# claude-code skill for OpenClaw

An [OpenClaw](https://github.com/openclaw/openclaw) skill for delegating coding tasks to the [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code).

## Features

- **Interactive PTY mode** — full terminal with confirmations, permissions, input
- **Headless pipe mode** — `-p` flag for automation, CI, structured JSON output
- **Session continuity** — `--continue` / `--resume SESSION_ID` across conversations
- **Parallel workflows** — git worktrees + multiple Claude Code processes
- **PR reviews** — safe temp-dir patterns, never in live workspace
- **Budget-capped automation** — `--max-budget-usd` for unattended runs
- **Granular tool restrictions** — `--allowedTools "Bash(git:*,npm:*),Read,Edit"`
- **Auto-notify** — `openclaw system event` wake trigger on completion
- **HANDOFF.md pattern** — context continuity across long sessions
- **Fan-out / Writer-Reviewer** — advanced parallel session patterns

## Install

### From ClawHub

```bash
openclaw skills install claude-code
```

### Local

```bash
git clone https://github.com/AtelyPham/claude-code-skill.git ~/clawd/claude-code
openclaw skills install --local ~/clawd/claude-code
```

## Requirements

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) (`claude` binary)
- OpenClaw with bash tool that supports `pty:true`

## License

MIT
