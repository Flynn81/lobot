---
name: quick-research
description: Rapidly verify a focused factual question using a small number of strong sources. Use for current facts, definitions, product or company facts, technical documentation, and other bounded research questions.
argument-hint: [question]
---

Answer this focused research question:

$ARGUMENTS

Use the minimum number of strong sources needed for confidence. Prefer primary or authoritative sources. If the answer is time-sensitive, prioritize current information.

Return:
- Answer
- Supporting evidence
- Source references
- Any important caveat or uncertainty

Do not expand the scope unless doing so changes the answer.
