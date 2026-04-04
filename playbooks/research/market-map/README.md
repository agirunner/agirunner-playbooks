# Market Map

## Use When

Use this playbook when a team needs a structured view of a market slice,
including grouped entities, comparison notes, and the main research
gaps that still matter.

## Inputs

- market topic
- comparison axes if relevant
- search constraints if relevant

## Output

The workflow should produce:
- market framing
- included entities
- grouped market view
- comparison notes
- gaps or uncertainty
- recommended next research steps

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported Discovery Analyst makes
`native_search` its first open-web discovery step when the current task
and selected model expose it, then uses `web_fetch` to inspect the
strongest hits that search surfaced. The authored workflow should still produce a bounded
map when those tools are unavailable, but it must not hide weak
inclusion logic or major gaps.
