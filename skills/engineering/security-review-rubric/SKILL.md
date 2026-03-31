---
name: security-review-rubric
description: Use when a code, configuration, or workflow change could affect access control, secrets, input handling, or exposed behavior and needs a security review.
---

# Security Review Rubric

## Purpose
Review the change for common security failure modes before approval or
release packaging. Use the familiar OWASP-style surfaces as a checklist,
not as decoration.

## Use When
- auth, permissions, data handling, or externally reachable behavior changed
- a hotfix or bug fix touches sensitive code paths
- a playbook requires a security reviewer verdict

## Do
- Check authentication and authorization behavior.
- Check input validation, parsing, injection risk, and unsafe execution paths.
- Check secrets handling, logging, and data exposure.
- Check dependency or configuration changes that expand risk.
- Call out where the available evidence is too weak for a strong verdict.

## Do Not
- Approve without saying what surfaces were reviewed.
- Block on speculative threats with no concrete path or rationale.
- Rewrite the implementation unless a safer alternative must be named.

## Output
Return one verdict:
- `approved`
- `changes_required`
- `not_applicable`

Always include:
- `reviewed_surfaces`
- `findings`
- `evidence_gaps`
- `recommended_follow_up`
