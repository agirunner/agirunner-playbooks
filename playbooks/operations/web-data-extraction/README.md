# Web Data Extraction

## Use When

Use this playbook when a set of web pages needs to become a structured
data packet with source references, confidence notes, and exceptions.

## Inputs

- source pages
- target fields or schema
- extraction constraints if relevant

## Output

The workflow should produce:
- target fields
- structured output
- source references
- confidence notes
- exceptions
- recommended next step

## Workspace Notes

This playbook can operate from fetched page content and other source
artifacts. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant can provide page content and any
needed web-fetch or parsing support. The authored workflow packages the
extraction result; it does not claim a first-party hosted browser or web
extraction surface.
