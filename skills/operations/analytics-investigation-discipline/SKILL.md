---
name: analytics-investigation-discipline
description: Use when a data question, query packet, or result set needs a bounded analytical answer with explicit caveats and safety assumptions.
---

# Analytics Investigation Discipline

## Purpose
Turn a data question or query packet into a bounded analysis with
explicit assumptions, caveats, and next-step guidance.

## Use When
- the workflow needs to answer a data question or review a query path
- the evidence may include schemas, query drafts, or result sets
- the final answer must preserve uncertainty and safety limits

## Do
- Restate the question, scope, and available data basis first.
- Keep query intent, actual evidence, and interpretation separate.
- Flag missing schema, thin coverage, and suspect assumptions.
- State what the analysis supports and what it does not support.
- Recommend safer next analysis when the current packet is too thin.

## Do Not
- Treat a vague metric request as if the data basis were obvious.
- Hide missing schema or query assumptions.
- Present a directional answer as precise fact.

## Output
- `analysis_scope`
- `data_basis`
- `query_or_logic_summary`
- `findings`
- `caveats`
- `recommended_next_step`
