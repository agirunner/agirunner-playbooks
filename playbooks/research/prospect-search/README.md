# Prospect Search

## Use When

Use this playbook when a team needs a ranked prospect packet against a
defined ideal profile, with evidence-backed fit notes and next-step
guidance.

## Inputs

- ideal profile
- market scope if relevant
- ranking rules if relevant

## Output

The workflow should produce:
- profile framing
- ranked candidates
- fit notes
- urgency signals
- risks or gaps
- recommended next actions

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported Account Discovery Analyst makes
`native_search` its first open-web discovery step when the current task
and selected model expose it, then uses `web_fetch` to inspect the
strongest hits that search surfaced. The authored workflow should still produce a smaller,
bounded packet when those tools are unavailable, but it must not
overstate ranking confidence.
