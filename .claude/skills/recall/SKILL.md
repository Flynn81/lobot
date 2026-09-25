---
name: recall
description: Retrieve relevant prior knowledge, decisions, research, projects, people, or meetings from the Obsidian memory vault.
argument-hint: "<question or topic to recall>"
context: fork
agent: memory-manager
---

Search durable memory for `$ARGUMENTS`.

Retrieve narrowly. Prefer canonical notes and explicit user decisions. Return:
- the relevant remembered context;
- note paths and dates;
- whether each important point is an explicit decision/fact, research finding, or inference;
- contradictions, uncertainty, or potentially stale information.

Do not modify the vault during recall.
