# Regression Monitor

## Use When

Use this playbook when a team needs an explicit regression-risk view of
a change or release candidate.

## Inputs

- change scope
- at-risk behavior
- available evidence if any

## Output

The workflow should produce:
- scoped behavior under review
- evidence reviewed
- coverage gaps
- regression risk
- recommended follow-up actions

## Workspace Notes

This playbook is storage-agnostic and can complete from artifacts or
repository evidence alone.

## Import Notes

This playbook is experimental and is intended to surface regression risk,
not to act as a full release gate by itself.
