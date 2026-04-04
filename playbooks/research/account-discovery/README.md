# Account Discovery

## Use When

Use this playbook when a team needs a qualification packet on a named
account or company, including fit, urgency, risk, and next-step
guidance.

## Inputs

- account name
- qualification goal if relevant
- search constraints if relevant

## Output

The workflow should produce:
- account summary
- fit signals
- urgency signals
- risks or gaps
- qualification level
- recommended next step

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported Account Discovery Analyst makes
`native_search` its first open-web discovery step when the current task
and selected model expose it, then uses `web_fetch` to inspect the
strongest hits that search surfaced. The authored workflow should still produce a bounded
qualification packet when those tools are unavailable, but it must
label evidence limits plainly.
