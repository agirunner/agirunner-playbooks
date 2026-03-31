# Catalog Authoring Guide

This repository is a curated import catalog for Agirunner. The authoring
goal is not to sketch ideas. The goal is to publish importable artifacts
that work as-is with minimal operator cleanup.

## Repository Contract

- Keep the repository content-only: YAML and Markdown only.
- Use category folders only for repository organization.
- Keep catalog IDs flat inside each artifact type.
- Keep imported fields inside the main artifact file when they are part
  of the live platform model.
- Keep README files focused on import decisions, usage guidance, and
  setup recommendations.

## Artifact Types

Skills:
- live at `skills/<category>/<slug>/SKILL.md`
- use standard frontmatter only: `name`, `description`
- keep content concise, reusable, and output-driven

Specialists:
- live at `specialists/<category>/<slug>/specialist.yaml`
- include metadata, tool contract, shared skill references, and the full
  `system_prompt`
- should be reusable across multiple playbooks

Playbooks:
- live at `playbooks/<category>/<slug>/playbook.yaml`
- include the full imported playbook shape plus catalog metadata
- store the full prose workflow contract in
  `definition.process_instructions`
- pair with `README.md` for import-time documentation

## Naming Rules

- Directory slug: lowercase kebab-case
- Catalog IDs: flat kebab-case, unique within each artifact type
- Display names: human-readable title case
- Avoid folder-shaped IDs such as `engineering/security-reviewer`

## Authoring Principles

- Prefer smaller reusable skills over huge specialist prompts.
- Prefer smaller reusable specialists over playbook-local role variants.
- Encode governance in prose, not declarative workflow policy fields.
- Make unhappy-path behavior explicit.
- Make storage behavior explicit when it changes the expected output.
- Write for importers who have not read the rest of this repository.

## Cross-Artifact References

- Playbooks reference specialists by catalog `id`.
- Specialists reference skills by catalog `id`.
- README guidance may mention recommended MCP or model setup, but that
  guidance is advisory and is not imported into the live playbook.

## Quality Bar

Do not merge artifacts that are:
- placeholders
- generic prompt dumps
- missing a concrete output contract
- missing closure guidance
- overly tied to a single repository layout or technology stack

Use these companion docs during review:
- `docs/playbook-quality-bar.md`
- `docs/skill-review-checklist.md`
- `docs/specialist-authoring-guide.md`
