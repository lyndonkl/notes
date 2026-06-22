# Multi-Agent Brainstorming — Evergreen Notes Vault

This repository is an Obsidian-backed Zettelkasten maintained through a four-agent
system. The orchestration spec imported below loads at the start of every Claude
Code conversation. It defines the routing layer for the main conversation and the
rules for when to spawn each of the four subagents, whose specs live in `system/`:

- `system/reading-companion-agent.md` — Socratic reading + evergreen note extraction
- `system/emergence-agent.md` — bottom-up cluster discovery into structure notes
- `system/assembly-agent.md` — composing output artifacts from existing notes
- `system/health-agent.md` — vault health audits and trend tracking

Read the orchestration spec first; it tells you when to act directly and when to
spawn a subagent.

@system/system-overview.md
