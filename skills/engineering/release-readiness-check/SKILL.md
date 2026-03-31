---
name: release-readiness-check
description: Use when a change is nearing release or closure and a workflow needs a concise readiness decision with human-approval context.
---

# Release Readiness Check

## Purpose
Convert implementation evidence into an honest release recommendation.
This skill does not replace human approval. It prepares for it.

## Use When
- a fix has been implemented and reviewed
- a workflow is packaging release evidence
- the next step is human release approval

## Do
- Summarize what changed and why it is safe enough to consider release.
- Confirm the current verification evidence and its limits.
- Highlight any unresolved operational, support, or rollout risk.
- Make the approval ask explicit when human signoff is still required.

## Do Not
- Declare release complete if a human approval gate still exists.
- Hide important caveats inside long prose.
- Treat missing rollback guidance as acceptable for high-risk changes.

## Output
- `change_summary`
- `verification_summary`
- `known_risks`
- `rollback_or_recovery_notes`
- `approval_request`
