---
name: deep-research
description: Conduct a thorough, evidence-backed investigation of a complex topic or question. Use when the answer requires multiple sources, conflicting evidence, current information, or substantial synthesis.
argument-hint: [research question]
context: fork
agent: researcher
background: false
---

Research the following question thoroughly:

$ARGUMENTS

Process:
1. Break the question into the smallest set of subquestions needed to answer it well.
2. Identify what is time-sensitive and verify those facts with current sources.
3. Prefer primary sources, official documentation, original data, peer-reviewed research, or direct statements when available.
4. Use high-quality secondary sources to add context and competing interpretations.
5. Cross-check consequential or surprising claims.
6. Record meaningful conflicts among credible sources.
7. Distinguish fact, interpretation, inference, and speculation.
8. Stop researching when additional sources are no longer likely to change the answer materially.

Return:
- Executive answer
- Key findings
- Evidence by subquestion
- Conflicting evidence / uncertainty
- Important gaps
- Sources
- Confidence and what could change it
