# Contributing

## Scope

This repository accepts community contributions for:
- shared skills
- shared specialists
- playbooks
- authoring docs
- catalog manifests

Do not add scripts, generators, or build-only infrastructure here.

## Contribution Rules

- Keep the repository content-only: YAML and Markdown only.
- Keep artifact IDs flat. Folder paths are for organization only.
- Do not add placeholder prompts or TODO sections.
- Do not add half-authored playbooks that require operator rewrite.
- Keep playbook launch inputs close to the current platform runtime shape.
- Do not reintroduce declarative governance fields such as
  `review_rules`, `assessment_rules`, `approval_rules`,
  `handoff_rules`, `checkpoints`, or `branch_policies`.
- Author workflow semantics in `process_instructions`.

## Adding A Skill

1. Create `skills/<category>/<slug>/SKILL.md`.
2. Use standard frontmatter only:
   - `name`
   - `description`
3. Keep the skill concise, reusable, and output-driven.
4. Register the skill in `catalog/skills.yaml`.

## Adding A Specialist

1. Create `specialists/<category>/<slug>/specialist.yaml`.
2. Author the full `system_prompt` in YAML.
3. Link only reviewed shared skills.
4. Register the specialist in `catalog/specialists.yaml`.

## Adding A Playbook

1. Create `playbooks/<category>/<slug>/playbook.yaml`.
2. Create `playbooks/<category>/<slug>/README.md`.
3. Author the full workflow contract in `process_instructions`.
4. Reference shared specialists by flat ID.
5. Register the playbook in `catalog/playbooks.yaml`.

## Review Checklist

Before proposing a new artifact, confirm:
- the scope is narrow and clear
- the output is reviewable
- unhappy-path behavior is explicit
- storage behavior is explicit when needed
- README import notes are useful and concise
- catalog manifests stay in sync

See [`docs/skill-review-checklist.md`](docs/skill-review-checklist.md)
and [`docs/playbook-quality-bar.md`](docs/playbook-quality-bar.md).
