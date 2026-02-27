# Claude Code Skill — Specs

Research and design specs for the OpenClaw Claude Code skill.

## Documents

| File | Content |
|------|---------|
| [research.md](research.md) | Raw findings from existing skills (`claude-code-mastery`, `openclaw-claude-code-skill`) |
| [features.md](features.md) | Feature inventory with priority tiers and scope decisions |
| [patterns.md](patterns.md) | Workflow patterns: parallel sessions, handoff, fan-out, writer/reviewer |
| [cli-reference.md](cli-reference.md) | Claude Code CLI flags, permission modes, tool restrictions |
| [architecture.md](architecture.md) | SKILL.md structure, frontmatter schema, file organization |

## Status

- [x] Research phase — analyzed 2 existing skills
- [x] SKILL.md v1 implementation (Tier 1 + Tier 2 complete)
- [ ] Testing / iteration
- [ ] Tier 3 features (`--fork-session`, `--from-pr`, `--output-format stream-json`, etc.)
- [ ] ClawHub publish
