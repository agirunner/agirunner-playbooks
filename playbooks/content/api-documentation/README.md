# API Documentation

## Use When

Use this playbook when an API or integration surface needs developer-
facing reference material that matches the actual contract.

## Not Ideal When

Do not use this playbook for end-user task guides, troubleshooting
articles, or broad conceptual product docs. Import
`technical-documentation` when the main job is to help a reader perform
an operational task rather than integrate against a request-response
contract.

## Inputs

- API surface in scope
- target reader
- source material context

## Output

The workflow should produce:
- source-truth basis
- request and response contract details
- authentication notes
- error notes
- examples
- important caveats
- unresolved contract questions if the source truth is incomplete
- editorial review findings

## Workspace Notes

This playbook works with a writable documentation workspace or in
advisory mode.

## Import Notes

The output quality is highest when the imported specialists can access
contract truth, implementation details, example payloads, and any
existing API docs. When those sources disagree or leave gaps, the
workflow should still end in a bounded reference draft with explicit
contract unknowns rather than implied guarantees.
