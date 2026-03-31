---
name: security-review-rubric
description: Use when a code, configuration, workflow, or agent behavior change could expand authority, expose data, ingest untrusted instructions, or weaken isolation and needs a security review.
---

# Security Review Rubric

## Purpose
Review the change using standard security expectations: least
privilege, clear trust boundaries, defense in depth, secure defaults,
and auditability. Focus on concrete exploit paths, blast radius, and
whether the current controls are strong enough for approval.

## Use When
- auth, permissions, secrets, network access, or exposed behavior changed
- the change adds or updates agent skills, prompts, memory, config, hooks, or workflow automation
- untrusted content can influence execution or tool use
- a hotfix, bug fix, or release candidate touches sensitive paths
- a playbook requires a security reviewer verdict

## Review Lens
Check these surfaces in order:
- provenance and trust: source, pinning, remote fetches, repo-controlled execution, and install or config side effects
- authority and blast radius: secrets, file writes, shell, network egress, privileged APIs, and shared credentials
- untrusted input handling: prompt injection, markdown or log ingestion, unsafe parsing, deserialization, and template or command injection
- isolation and containment: sandboxing, writable scope, network restrictions, host escape paths, and tenant spillover
- governance and recovery: approvals, audit logs, inventory, rollback or revocation path, and incident visibility
- high-risk combination: sensitive data access, untrusted content, and outbound communication in the same flow

## Do
- Name the reviewed surfaces and the evidence actually used.
- Separate proven issues from plausible concerns.
- Prefer the smallest concrete mitigation that materially reduces risk.
- Call out where the available evidence is too weak for a strong verdict.

## Do Not
- Approve without tracing authority, data flow, and execution paths.
- Block on speculative threats without an attack path or missing control.
- Assume scanning alone is enough; read the instructions and behavior.
- Ignore governance gaps just because one code path looks safe.

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
