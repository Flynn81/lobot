---
name: memory-management
description: Organize durable notes about decisions, preferences, projects, open questions, and important findings. Use when asked to remember, reconcile, update, prune, or summarize long-lived assistant context.
argument-hint: [memory task]
---

Manage durable notes for this request:

$ARGUMENTS

For each candidate note, ask whether it is likely to matter in a future session. Prefer concise facts that alter future recommendations or save repeated explanation.

Use this shape when practical:
- Topic
- Durable fact / decision
- Why it matters
- Date / provenance if relevant
- Status: active / superseded / tentative
- Review or expiry condition, if the information can become stale

When reconciling notes:
- preserve the newest authoritative information;
- flag contradictions instead of silently merging them;
- mark superseded information;
- remove duplication;
- avoid storing transient chatter or unnecessarily sensitive detail.
