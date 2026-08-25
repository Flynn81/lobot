---
name: fact-check
description: Verify one or more factual claims and identify whether each is supported, misleading, unverified, or contradicted. Use for numerical, current, surprising, disputed, or consequential claims.
argument-hint: [claim or claims]
---

Fact-check the following:

$ARGUMENTS

For each material claim:
1. Parse the exact claim, including date, scope, quantity, and qualifiers.
2. Find the best available evidence.
3. Determine whether the evidence actually supports the precise wording.
4. Check for stale data, omitted context, or stronger contrary evidence.

Use one of these verdicts:
- Verified
- Mostly verified
- Misleading / missing context
- Unverified
- Contradicted

Provide a corrected formulation for any claim that is misleading or wrong.
