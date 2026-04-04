---
name: research-methodology
description: Use when a workflow needs disciplined research, synthesis, source comparison, and honest confidence statements.
---

# Research Methodology

## Purpose
Keep research grounded in explicit questions, sources, evidence quality,
and unresolved uncertainty.

## Use When
- the task requires external research or source synthesis
- the answer will drive a recommendation or decision
- conflicting sources must be reconciled

## Do
- Start with the exact research question.
- Use `tool_search` with exact tool ids or names, beginning with `native_search` and `web_fetch` when relevant, to confirm the current task's exposed tool list before deciding which research surfaces are actually available.
- If `native_search` is exposed and the brief or task inputs say to prefer quoted `native web search`, use quoted `native web search` before starting open-web discovery with `web_fetch`.
- Prefer primary or direct sources where possible.
- Use a clear source hierarchy: primary first, direct secondary next, tertiary only with caution.
- Track source recency explicitly when the topic can change quickly.
- Weigh source quality explicitly when primary evidence is unavailable.
- Compare sources instead of stopping at the first plausible answer.
- Mark what is confirmed, inferred, and still unknown.
- State confidence honestly.

## Do Not
- Claim `native_search` or quoted `native web search` is unavailable after only a vague natural-language `tool_search` miss; check exact tool ids or names first.
- Carry a stale tool-availability note from an earlier artifact forward when the current task exposes a different tool set.
- Blend facts and interpretation without labeling them.
- Ignore contradictory evidence.
- Pretend weak sources support a strong conclusion.

## Output
- `research_question`
- `sources_consulted`
- `source_quality_notes`
- `findings`
- `contradictions_or_gaps`
- `confidence`
- `recommended_next_step`
