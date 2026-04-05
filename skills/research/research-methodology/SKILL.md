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
- Treat `native_search` as a provider-managed capability rather than a normal callable runtime tool. After `tool_search` confirms it is available, continue with the actual research question so the provider can invoke search in the next model turn.
- Prefer primary or direct sources where possible.
- Use a clear source hierarchy: primary first, direct secondary next, tertiary only with caution.
- Track source recency explicitly when the topic can change quickly.
- Weigh source quality explicitly when primary evidence is unavailable.
- Compare sources instead of stopping at the first plausible answer.
- List outside sources as `sources_consulted` only when you actually retrieved them in the current task through `native_search`, `web_fetch`, provided artifacts, MCP, or another exposed retrieval path.
- Mark what is confirmed, inferred, and still unknown.
- State confidence honestly.

## Do Not
- Claim `native_search` or quoted `native web search` is unavailable after only a vague natural-language `tool_search` miss; check exact tool ids or names first.
- Carry a stale tool-availability note from an earlier artifact forward when the current task exposes a different tool set.
- Re-check tool availability repeatedly and then fall back to shell-only or memory-only synthesis while `native_search` is available for the question.
- Cite source names, publication dates, or source-quality claims from memory as though they were retrieved in the current task.
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
