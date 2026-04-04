# Research Brief To Report

## Use When

Use this playbook when a team needs a research brief turned into a
reviewed report that another operator or decision-maker can read
directly.

## Inputs

- research brief
- target audience if relevant
- source constraints if relevant

## Output

The workflow should produce:
- brief framing
- sources consulted
- report draft
- caveats and contradictions
- review findings or disposition
- final recommendation framing

## Workspace Notes

This playbook can operate entirely from artifacts and external research
access. It does not require a writable code workspace.

## Import Notes

Best results come when the imported Research Analyst and Research
Reviewer make `native_search` the first open-web discovery step when
the current task and selected model expose it, then use `web_fetch` to
inspect the strongest hits that search surfaced. The authored workflow should
still function without those tools, but it must narrow the report and
label unsupported areas explicitly.
