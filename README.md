# Claude Code Personal Chief of Staff Starter Kit

This starter kit turns Claude Code into a lightweight digital chief of staff and research assistant using first-class Claude Code extension points:

- `CLAUDE.md` for always-on behavior and standards
- custom subagents for isolated research, analysis, criticism, and verification
- skills for reusable workflows

## Included structure

```text
.claude/
├── CLAUDE.md
├── agents/
│   ├── researcher.md
│   ├── analyst.md
│   ├── critic.md
│   └── fact-checker.md
└── skills/
    ├── deep-research/SKILL.md
    ├── quick-research/SKILL.md
    ├── fact-check/SKILL.md
    ├── decision-analysis/SKILL.md
    ├── compare-options/SKILL.md
    ├── devils-advocate/SKILL.md
    ├── meeting-prep/SKILL.md
    ├── research-report/SKILL.md
    ├── daily-brief/SKILL.md
    └── memory-management/SKILL.md
```

## Install as a personal, user-wide assistant

Copy the contents of `.claude/` into your user-level Claude directory:

```bash
mkdir -p ~/.claude
cp -R .claude/* ~/.claude/
```

If you already have a `~/.claude/CLAUDE.md`, merge the contents rather than overwriting it.

## Install for only one project

Copy `.claude/` into the root of that project instead. Project-level definitions are useful if the assistant should have project-specific behavior, while user-level definitions follow you across projects.

## Suggested usage

Natural-language delegation works, for example:

```text
Use the researcher agent to investigate the current options for local-first note-taking apps.
```

or explicitly invoke a skill:

```text
/deep-research What are the strongest approaches to building a personal knowledge assistant with Claude Code?
```

```text
/decision-analysis Should I use MCP, local files, or a vector database as the main memory layer for my assistant?
```

```text
/devils-advocate Stress-test this architecture before I implement it.
```

Claude Code can also discover appropriate skills automatically from their descriptions.

## Recommended operating pattern

For complex questions:

```text
You
 ↓
Main Claude session / Chief of Staff
 ├─ researcher → evidence
 ├─ analyst → tradeoffs and recommendation
 ├─ critic → challenge and failure modes
 └─ fact-checker → verify important claims
 ↓
Main Claude synthesizes the final answer
```

The goal is not to invoke every agent every time. The main assistant should use them when specialization or isolated context materially improves the answer.

## Why `deep-research` uses a forked context

The `deep-research` skill uses `context: fork` with the `researcher` agent. That keeps a large research process out of the main conversation context and returns the result for synthesis.

This is useful for investigations that read many sources or generate substantial intermediate material.

## Suggested next additions

Once the core setup works well, consider adding:

1. MCP connections for services you actually use, such as browser/search, Google Drive, Gmail, Calendar, Slack, GitHub, Notion, or databases.
2. A local knowledge directory (for example `~/assistant-knowledge/`) with durable project notes and decision records.
3. A writing/editor agent for polished memos, emails, PRDs, and presentations.
4. A planner agent for project decomposition and follow-through.
5. Hooks only for deterministic behavior that must always occur, rather than judgment-based workflows.
6. A plugin package once you want to reuse or distribute the complete setup.

## Tuning tips

- Keep `CLAUDE.md` short and focused on instructions that should apply every session.
- Give skills specific descriptions so Claude can select them correctly.
- If a skill triggers too often, narrow its description or make it manual-only.
- Add new skills when you notice yourself repeating the same prompt or workflow.
- Add a subagent when a specialized side task floods the main context or benefits from independent reasoning.
- Add MCP when the assistant repeatedly needs information from a service it cannot access directly.
- Add hooks for deterministic enforcement or automation, not for tasks that require judgment.

## Compatibility note

This kit was authored against Claude Code documentation current as of August 2026. Claude Code evolves quickly, so re-check frontmatter fields and tool names if you are using a substantially older or newer version.
