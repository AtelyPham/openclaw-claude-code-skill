# Feature Inventory

Priority tiers for the Claude Code skill. Scope decisions based on research.

---

## Tier 1 — Core (v0.1.0, ship first)

Must-haves for the skill to be useful. Already in current SKILL.md.

| Feature | Status | Notes |
|---------|--------|-------|
| PTY mode (`pty:true`) | ✅ Done | Interactive terminal, confirmations |
| Headless pipe mode (`-p`) | ✅ Done | Automation, JSON output |
| Permission modes | ✅ Done | `default`, `acceptEdits`, `plan`, `bypassPermissions` |
| Session continuity | ✅ Done | `--continue`, `--resume SESSION_ID` |
| Key CLI flags reference | ✅ Done | Comprehensive flag table |
| Background task monitoring | ✅ Done | `process` tool actions |
| Safety rules | ✅ Done | 10 rules covering common pitfalls |
| Auto-notify on completion | ✅ Done | `openclaw system event` trigger |
| Budget-capped automation | ✅ Done | `--max-budget-usd` |
| Granular tool restrictions | ✅ Done | `--allowedTools "Bash(git:*),Read,Edit"` |

## Tier 2 — Patterns (v0.2.0)

Workflow patterns that make the skill more powerful.

| Feature | Status | Notes |
|---------|--------|-------|
| HANDOFF.md pattern | ✅ Done | Context continuity across long sessions |
| Parallel worktrees | ✅ Done | Multiple issues in parallel |
| Fan-out pattern | ✅ Done | Bulk `claude -p` over file list |
| Writer/Reviewer pattern | ✅ Done | Dual sessions: implement + review |
| PR review (safe temp dir) | ✅ Done | Clone-to-tmpdir pattern |
| Inline subagents (`--agents`) | ✅ Done | JSON agent definitions, no files |
| Progress update guidelines | ✅ Done | When/how to inform user |

## Tier 3 — Polish (v0.3.0+)

Nice-to-haves for later.

| Feature | Status | Notes |
|---------|--------|-------|
| `--fork-session` flag | ✅ Done | Branch a session when resuming for risky exploration |
| `--resume` search | ✅ Done | Interactive session picker with optional search term |
| `--output-format stream-json` | ✅ Done | Real-time streaming output (not `--stream`) |
| `--append-system-prompt` vs `--system-prompt` | ✅ Done | Document the distinction |
| `--from-pr` flag | ✅ Done | Resume session linked to a PR by number/URL |

## Explicitly Out of Scope

| Feature | Reason |
|---------|--------|
| Subagent team (11 roles) | Over-engineered; user defines own agents |
| Self-improving heartbeat/cron | Too complex, fragile |
| claude-mem integration | External dep, separate concern |
| Setup scripts | OpenClaw handles install via `metadata.openclaw.install` |
| MCP server management | Separate tool |
| Multi-model proxy routing | Edge case |
| Multi-device session sync | Out of scope |
| Quick-check gate | `requires.bins` already checks for `claude` binary |
| Test-First pattern | Behavior customization; skill scope is teaching CLI usage, not changing Claude Code behavior |
| Diff-first display | Behavior customization; telling Claude Code how to display output |
