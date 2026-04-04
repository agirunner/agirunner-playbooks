# Contract Term Extraction

## Use When

Use this playbook when a contract needs to become a structured term
packet with clause support and explicit ambiguity notes.

## Inputs

- contract source
- target terms if relevant
- normalization rules if relevant

## Output

The workflow should produce:
- target terms
- structured term output
- supporting clauses or evidence notes
- ambiguity notes
- exceptions
- recommended next step

## Workspace Notes

This playbook can operate from uploaded contracts, extracted text, and
other source artifacts. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant can provide contract content and
any needed parsing support. The authored workflow packages extraction
and review; it does not claim first-party legal or extraction product
surfaces beyond that.
