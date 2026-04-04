# SQL Investigation

## Use When

Use this playbook when a data question needs a bounded SQL or
query-driven investigation packet with findings and caveats.

## Inputs

- investigation question
- data scope if relevant
- query constraints if relevant

## Output

The workflow should produce:
- analysis scope
- data basis
- query or logic summary
- findings
- caveats
- recommended next step

## Workspace Notes

This playbook can operate from schema notes, query packets, result sets,
and other evidence artifacts. It does not require a writable code
workspace.

## Import Notes

Import this playbook when your tenant can supply SQL or data-access
tooling through its own bindings or artifacts. The authored workflow
packages the investigation outcome and does not imply a first-party
hosted SQL execution product.
