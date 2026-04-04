# Document Extraction

## Use When

Use this playbook when a document needs to become a structured field
packet with evidence notes and explicit exception handling.

## Inputs

- source document
- target fields or schema
- normalization rules if relevant

## Output

The workflow should produce:
- target schema or fields
- structured output
- evidence notes
- ambiguous fields
- exceptions
- recommended next step

## Workspace Notes

This playbook can operate from uploaded documents, extracted text, and
other source artifacts. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant can provide document content and
any needed extraction tooling or parsing support. The authored workflow
is packaging-first: it produces a bounded extraction packet and does not
assume a first-party hosted extraction substrate.
