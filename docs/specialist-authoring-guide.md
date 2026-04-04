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
- tell the specialist when to pause, route back, or escalate rather than
  invent missing facts

Escalation, rework, and closure expectations should live in the specialist
prompt and the playbook prose, not in speculative specialist metadata that
the platform does not actually own today.

## Tool Contract Standard

Most specialists should declare:

```yaml
allowed_tools: all-specialist-tools
```

That shared profile is defined in `catalog/tool-profiles.yaml` and
should include every specialist-safe tool while excluding orchestrator-
only tools. When a specialist category needs a different shared default,
use another named profile from `catalog/tool-profiles.yaml`. Use an
explicit array only when the specialist truly needs a smaller tool
surface than the available shared profiles.

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
