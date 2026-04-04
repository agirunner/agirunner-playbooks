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
- describe what good execution looks like when the needed evidence,
  tools, and workspace access are available
- define what evidence or artifacts must be produced
- define what the specialist must not do
- tell the specialist how to behave when the workspace is writable
  versus advisory-only
- tell the specialist what to do when the strongest path is blocked by
  weak inputs, missing context, unavailable tools, or contradictory
  evidence
- tell the specialist when to pause, route back, or escalate rather than
  invent missing facts

Escalation, rework, and closure expectations should live in the specialist
prompt and the playbook prose, not in speculative specialist metadata that
the platform does not actually own today.

## Tool Contract Standard

Most specialists should declare a named shared profile from
`catalog/tool-profiles.yaml`:

```yaml
allowed_tools: read-only-review-tools
```

Those shared profiles are defined in `catalog/tool-profiles.yaml`.
Choose the narrowest profile that still lets the specialist do its job.
When a specialist category needs a different shared default, use another
named profile from `catalog/tool-profiles.yaml`. Use an explicit array
only when the specialist truly needs a smaller tool surface than the
available shared profiles.

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
