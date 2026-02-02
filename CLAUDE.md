# CLAUDE.md — intel-skill

Market intelligence CLI skill for Claude Code / AI agents.

## Stack
- Bash scripts
- SKILL.md defines the interface
- No build step, no package manager

## Conventions
- 8 research modes (see SKILL.md)
- Scripts must work standalone (no external deps beyond curl/jq)
- Keep outputs concise — this runs inside agent context windows
- Conventional commits
