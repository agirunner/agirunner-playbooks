---
name: api-reference-writing
description: Use when API endpoints, contracts, or developer-facing integration details must be documented clearly for implementation or support use.
---

# API Reference Writing

## Purpose
Produce reference material that helps readers integrate correctly without
guessing hidden rules.

## Use When
- documenting an API or webhook surface
- turning implementation knowledge into reference docs
- updating docs after request or response changes

## Do
- State what the endpoint does and when to use it.
- Document inputs, outputs, auth, and error shapes.
- Keep examples consistent with the declared contract.
- Surface environment, versioning, and prerequisite assumptions when they matter.
- Include concrete examples when they clarify the contract.
- Separate reference facts from opinionated usage guidance.

## Do Not
- Hide required parameters in examples only.
- Assume internal knowledge about auth or environment setup.
- Let examples contradict field names, required flags, or error behavior.
- Describe unstable behavior as a firm contract.

## Output
- `endpoint_summary`
- `request_contract`
- `response_contract`
- `authentication_notes`
- `error_notes`
- `example_requests_or_responses`
