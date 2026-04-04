# Research Analysis

## Use When

Use this playbook when a team needs a grounded answer to a specific
research question, along with source-based findings and honest
confidence.

## Inputs

- research question
- decision context if relevant
- source scope or source constraints if relevant

## Output

The workflow should produce:
- research question framing
- sources consulted
- findings
- contradictions or gaps
- confidence
- recommendation or next step

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported research specialist makes
`native_search` its first open-web discovery step when the current task
and selected model expose it, then uses `web_fetch` to inspect the
strongest hits that search surfaced. The authored Research Analyst
guidance requires that search-first flow, but the workflow should still
function with documented source limits if it is not configured, not
enabled, or does not surface the needed evidence.
