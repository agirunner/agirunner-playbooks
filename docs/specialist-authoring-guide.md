# Specialist Authoring Guide

Shared specialists are reusable worker definitions. They should be
useful across multiple playbooks without becoming so generic that they
stop being trustworthy.

## Specialist File Contract

Each `specialist.yaml` should include:
- `id`
- `name`
- `category`
- `stability`
- `description`
- `allowed_tools`
- `skill_ids`
- `verification_strategy`
- `escalation_target`
- `max_escalation_depth`
- `is_active`
- `system_prompt`

## Prompt Standard

The `system_prompt` should:
- state the specialist role clearly
- tell the specialist to read the workflow goal, parameters, and current
  workspace before acting
- define what evidence or artifacts must be produced
- define what the specialist must not do
- tell the specialist how to behave when the workspace is writable
  versus advisory-only
- tell the specialist when to escalate rather than invent missing facts

## Reuse Standard

Prefer shared skills for reusable techniques such as:
- security review
- regression proof
- technical writing
- research methodology

Do not bury reusable technique guidance inside every specialist prompt.

## Avoid

Reject specialists that:
- depend on one specific playbook to make sense
- hardcode repo-specific filenames as if they were universal
- assume git-only workspaces
- rely on operator memory instead of explicit output contracts
