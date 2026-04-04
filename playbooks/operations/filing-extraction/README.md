# Filing Extraction

## Use When

Use this playbook when a filing needs to become a structured field
packet with evidence notes, normalization notes, and exceptions.

## Inputs

- filing source
- target fields or schema
- normalization rules if relevant

## Output

The workflow should produce:
- target fields
- structured output
- evidence notes
- normalization notes
- exceptions
- recommended next step

## Workspace Notes

This playbook can operate from uploaded filings, extracted text, and
other source artifacts. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant can provide filing content and any
needed parsing support. The authored workflow is packaging-first and
does not assume a first-party hosted filing-extraction substrate.
