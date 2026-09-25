---
name: remember
description: Extract durable knowledge from the current work and propose or write it to the Obsidian memory vault.
argument-hint: "[what to remember, or leave blank to inspect current context]"
---

Identify durable information worth preserving from the current work. Do not save transient chatter or whole conversations.

1. Determine the memory type: project, decision, research, person, organization, topic, meeting, or other durable context.
2. Search the Obsidian vault for an existing canonical note.
3. Draft the smallest useful update, with provenance/date and relevant `[[wikilinks]]`.
4. If an existing memory conflicts, preserve and flag the contradiction.
5. Unless the user has explicitly authorized automatic memory writes, show the proposed create/update and ask for approval before writing.
6. If approved (or auto-write is authorized), make the change and report the path changed.

Never store passwords, API keys, tokens, or other credentials.
