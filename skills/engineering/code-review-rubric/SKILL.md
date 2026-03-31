---
name: code-review-rubric
description: Use when reviewing a proposed code or configuration change for correctness, maintainability, and release safety before approval.
---

# Code Review Rubric

## Purpose
Review the proposed change itself, not the author. Focus on correctness,
clarity, architectural fit, tests, and release risk.

## Use When
- a bug fix or code change is ready for review
- a playbook stage needs an approval or request-changes decision
- a reviewer needs a consistent bar across multiple repositories

## Do
- Check whether the change solves the stated problem.
- Review the change in the context of surrounding files, interfaces, and authored behavior, not as an isolated diff.
- Review across the standard dimensions that usually matter: correctness,
  testability, maintainability, security, performance, and operability.
- Check whether the change fits the existing architecture and boundary patterns instead of only working locally.
- Check whether tests or other verification actually cover the changed
  behavior.
- Check whether docs, examples, API expectations, or migration assumptions stay accurate where the change affects them.
- Check whether names, boundaries, and side effects remain readable.
- Check for missing edge cases, rollout risks, or hidden assumptions.
- Distinguish blocking findings from non-blocking improvements and make the severity obvious.

## Do Not
- Block on personal style preferences without a real correctness or
  maintainability risk.
- Approve without naming what was reviewed.
- Treat an unverified assumption as if it were confirmed behavior.
- Ask for broad unrelated refactors inside a narrow change.

## Output
Return one verdict:
- `approved`
- `changes_required`
- `rejected`

Always include:
- `review_scope`
- `blocking_findings`
- `non_blocking_callouts`
- `open_questions_or_assumptions`
- `verification_gaps`
