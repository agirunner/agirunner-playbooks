# Vendor Evaluation

## Use When

Use this playbook when a team needs a structured vendor comparison tied
to explicit requirements, constraints, and decision criteria.

## Inputs

- decision scope
- evaluation criteria
- candidate vendors
- constraints or context if available

## Output

The workflow should produce:
- evaluation criteria
- vendor comparison
- material risks
- unknowns
- recommendation or shortlist

## Workspace Notes

This playbook is storage-agnostic and usually relies more on research
access than on writable repository access.

## Import Notes

If external research providers are configured for the imported
specialists, especially when the current task and selected model expose
the `native_search` tool for quoted `native web search`, the output
quality improves materially when it is the first open-web discovery step
and `web_fetch` is used afterward to inspect the strongest sources that
search surfaced. The workflow should still complete honestly when
source access is limited or that tool is not enabled.
