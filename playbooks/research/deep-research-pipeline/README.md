# Deep Research Pipeline

## Use When

Use this playbook when a team needs multi-pass research that ends in a
reviewed synthesis, not just a quick source summary.

## Inputs

- research brief
- decision goal if relevant
- source constraints if relevant

## Output

The workflow should produce:
- brief framing
- sources consulted
- source quality notes
- synthesis draft
- review findings or disposition
- final recommendation

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported Research Analyst and Research
Reviewer make `native_search` the first open-web discovery step when
the current task and selected model expose it, then use `web_fetch` to
inspect the strongest hits that search surfaced. The authored workflow should
still function without those tools, but it must narrow the conclusion
and label evidence limits plainly.
