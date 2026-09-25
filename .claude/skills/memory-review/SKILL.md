---
name: memory-review
description: Audit the Obsidian memory vault for duplicates, contradictions, stale notes, orphaned notes, unresolved decisions, and inbox items needing consolidation.
argument-hint: "[optional folder, project, or topic scope]"
context: fork
agent: memory-manager
---

Review memory within `$ARGUMENTS` if supplied; otherwise perform a bounded health review rather than loading the entire vault blindly.

Check for duplicate canonical notes, contradictions, stale facts, orphaned/unlinked notes, unresolved decisions/open questions, and `90 Inbox` items that should be consolidated.

Return a prioritized maintenance plan. Do not delete or rewrite substantive memory without explicit approval.
