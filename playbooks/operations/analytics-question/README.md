# Analytics Question

## Use When

Use this playbook when a stakeholder analytics question needs a bounded
answer packet with the data basis and caveats preserved.

## Inputs

- stakeholder question
- data scope if relevant
- decision context if relevant

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

Import this playbook when your tenant can supply the relevant data basis
through its own query tooling or artifacts. The authored workflow
packages the answer and does not imply a first-party hosted analytics
surface.
