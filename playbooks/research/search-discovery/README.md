# Search Discovery

## Use When

Use this playbook when a team needs a scoped discovery packet instead of
one final answer, such as source discovery, signal discovery, or a
ranked set of candidate findings.

## Inputs

- discovery brief
- target scope if relevant
- search constraints if relevant

## Output

The workflow should produce:
- discovery brief framing
- search scope
- ranked or grouped findings
- supporting evidence
- gaps or uncertainty
- recommended next step

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported Discovery Analyst can use the quoted
`native web search` tool for the task or an equivalent external research
integration. The authored workflow should still function with a smaller
packet and explicit search limits when those tools are unavailable.
