# Playbook Quality Bar

Community playbooks must meet the same specificity bar as the live
platform test corpus. The orchestrator should be able to run the
workflow from authored prose without relying on hidden governance
config, brittle string matching, or operator guesswork.

## Required Content

Every playbook MUST include:
- a clear outcome
- a stable catalog `id`
- a human-readable `version`
- explicit launch parameters
- explicit board columns
- explicit stages with named specialists
- a complete `definition.process_instructions`
- a `README.md` that helps an operator decide whether to import it

## Process Instructions Standard

`definition.process_instructions` MUST:
- name the authored stages literally
- name the participating specialists literally
- describe the preferred flow
- describe recovery and exception handling
- define completion rules
- define stage-specific closure rules when the stage contract is not
  obvious
- include guided-closure language that keeps the workflow moving when
  closure is still legally possible
- avoid invented tenant-specific assignee language unless the named
  target is one of the authored specialists

## Storage Standard

Playbooks MUST support the workspace types the platform can expose:
- `git`
- `host_directory`
- `artifact`

Playbooks MAY author storage-specific behavior in prose when the output
changes across those modes. For example:
- `git`: mutate code, verify, and push
- `host_directory`: mutate in place and produce evidence without git-only
  packaging assumptions
- `artifact`: complete in advisory mode with diagnosis, proposed patch,
  and verification guidance

## What To Avoid

Reject playbooks that:
- depend on declarative governance fields for approvals or rework
- depend on folder names or category labels in runtime behavior
- assume only git-backed workspaces exist
- assume an operator will rewrite prompts after import
- overpromise autonomous feature delivery when the safer scope is a
  narrow, human-gated workflow

## SDLC Guidance

Narrow SDLC playbooks are allowed and useful. They SHOULD stay focused
on bounded flows such as:
- bug fix
- hotfix
- code review
- PR guardian
- regression monitor

Broad autonomous feature-delivery playbooks SHOULD NOT be curated as
default imports until the platform maturity justifies them.
