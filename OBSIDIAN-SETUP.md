# Obsidian persistent-memory setup

1. Open `Obsidian-Vault/` as a vault in Obsidian, or copy its folders/templates into an existing vault.
2. Give Claude Code access to the vault when launching it, for example:
   `claude --add-dir "/path/to/your/Obsidian-Vault"`
3. Copy/merge this kit's `.claude/` into `~/.claude/` for global use, or into a project's `.claude/` for project-only use.
4. Start with approval-gated writes. Use `/remember` to propose durable memories and `/recall` to retrieve them.
5. Periodically run `/memory-review` on a project/topic or on the inbox.

## Recommended operating model

- `CLAUDE.md`: durable behavior and memory policy.
- Claude auto-memory: Claude Code/project operational learnings.
- Obsidian: curated long-term knowledge, decisions, research, meetings, people, and projects.
- `memory-manager`: retrieval/consolidation specialist.

## Good first test

Ask Claude to create a project note for the assistant itself, approve it, then run `/recall` in a new session and verify it finds the decision and provenance without loading unrelated notes.
