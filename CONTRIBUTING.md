# Contributing to Agirunner Playbooks

Thanks for contributing.

This repository owns the shared community catalog for Agirunner:
importable playbooks, specialists, skills, catalog manifests, and
catalog authoring guidance.

If your change is primarily about dashboard behavior, API import flows,
or other control-plane product semantics, it probably belongs in
[`agirunner-platform`](https://github.com/agirunner/agirunner-platform),
not here.

If your change is primarily about agent execution, workspace
materialization, tool transport, or runtime-side behavior, it probably
belongs in
[`agirunner-runtime`](https://github.com/agirunner/agirunner-runtime),
not here.

For the broader multi-repo contribution overview, see
[`agirunner/CONTRIBUTING.md`](https://github.com/agirunner/agirunner/blob/main/CONTRIBUTING.md).

If you are looking for the main product entry point, start with
[`agirunner`](https://github.com/agirunner/agirunner). Product and
operator documentation lives at
[`docs.agirunner.dev`](https://docs.agirunner.dev).

Useful docs entry points:

- [Getting Started](https://docs.agirunner.dev/getting-started/introduction/)
- [Playbooks And Authoring](https://docs.agirunner.dev/dashboard/playbooks-and-authoring/)
- [Dashboard Overview](https://docs.agirunner.dev/dashboard/overview/)
- [Platform Overview](https://docs.agirunner.dev/platform/overview/)

## Scope

Contributions are welcome for:
- shared skills
- shared specialists
- playbooks
- catalog manifests
- authoring and review documentation

Do not add scripts, generators, build pipelines, or runtime code here.
This repository should stay content-only.

## General Rules

- Keep the repository YAML-and-Markdown only.
- Keep artifact IDs flat. Folder paths are for organization only.
- Keep imported fields aligned with the live platform model.
- Keep catalog-facing identity metadata explicit and consistent.
- Do not add placeholder prompts, TODO sections, or half-authored
  playbooks.
- Keep playbook launch inputs close to the current platform runtime
  shape.
- Author workflow governance in `definition.process_instructions`.
- Do not reintroduce declarative governance fields such as
  `review_rules`, `assessment_rules`, `approval_rules`,
  `handoff_rules`, `checkpoints`, or `branch_policies`.
- Keep the dated catalog history in [`CHANGELOG.md`](CHANGELOG.md)
  current when the visible catalog changes.

## Quality Expectations

- Skills should stay concise, usually at or under 100 lines.
- Skills should use standard industry techniques or quality bars where
  that helps the specialist act more consistently.
- Specialists should be reusable across multiple playbooks.
- Playbooks should be import-ready, not templates waiting for an
  operator rewrite.
- Experimental engineering playbooks should stay narrow and
  human-gated.

## Shared Tool Contract

Most specialists should declare:

```yaml
allowed_tools: all-specialist-tools
```

That profile is defined in [`catalog/tool-profiles.yaml`](catalog/tool-profiles.yaml).
Use another named shared profile from that file when a category needs a
different default tool surface. Use an explicit tool list only when the
specialist truly needs a smaller tool surface than the available shared
profiles.

## Adding Or Updating A Skill

1. Create or update `skills/<category>/<slug>/SKILL.md`.
2. Use only the standard frontmatter keys:
   - `name`
   - `description`
3. Keep the content reusable, output-driven, and concise.
4. Register or update the artifact in [`catalog/skills.yaml`](catalog/skills.yaml).

Before considering the skill ready, confirm:
- the scope is narrow and reusable
- the output shape is explicit
- the content is not copied verbatim from third-party skills
- the skill does not hide playbook-specific governance

## Adding Or Updating A Specialist

1. Create or update `specialists/<category>/<slug>/specialist.yaml`.
2. Store the full `system_prompt` inline in YAML.
3. Default to a named shared tool profile from `catalog/tool-profiles.yaml`
   unless a tighter explicit restriction is truly needed.
4. Reference only reviewed shared skills.
5. Register or update the artifact in
   [`catalog/specialists.yaml`](catalog/specialists.yaml).

Before considering the specialist ready, confirm:
- the prompt defines output expectations clearly
- storage behavior is explicit when advisory mode matters
- the specialist does not depend on one single playbook to make sense

## Adding Or Updating A Playbook

1. Create or update `playbooks/<category>/<slug>/playbook.yaml`.
2. Create or update `playbooks/<category>/<slug>/README.md`.
3. Set an explicit `author` value in both the playbook file and
   [`catalog/playbooks.yaml`](catalog/playbooks.yaml).
4. Author the full workflow contract in
   `definition.process_instructions`.
5. Reference shared specialists by flat catalog ID.
6. Register or update the artifact in
   [`catalog/playbooks.yaml`](catalog/playbooks.yaml).

Playbook prose should normally include:
- `Preferred flow`
- `Recovery and exception handling`
- `Completion rules`
- `Guided closure rule`

Before considering the playbook ready, confirm:
- the scope is narrow and clear
- the author field is correct for the catalog entry and playbook file
- the named stages are explicit
- the recovery path is explicit
- storage behavior is honest for `git`, `host_directory`, and `artifact`
  contexts when relevant
- the README helps an operator decide whether to import it

## Keep The Catalog In Sync

When you add or rename an artifact, update the related manifest in the
same logical change:
- [`catalog/skills.yaml`](catalog/skills.yaml)
- [`catalog/specialists.yaml`](catalog/specialists.yaml)
- [`catalog/playbooks.yaml`](catalog/playbooks.yaml)

For playbooks, treat these metadata fields as a sync set between the
manifest and the underlying `playbook.yaml`:
- `id`
- `name`
- `author`
- `category`
- `stability`
- `version`

If you change authoring expectations or contributor workflow, update the
root docs in the same change:
- [`README.md`](README.md)
- [`CONTRIBUTING.md`](CONTRIBUTING.md)
- [`CHANGELOG.md`](CHANGELOG.md)

## Validation Checklist

Before considering a content change ready, confirm:

- the touched artifact imports cleanly into the live platform model
- the matching catalog manifest entry is present and aligned
- the visible author, category, stability, and version fields are
  consistent where required
- playbook README guidance is still accurate for operators deciding
  whether to import it
- the dated changelog entry reflects the catalog change

## Review References

Use these docs during review:
- [`docs/catalog-authoring-guide.md`](docs/catalog-authoring-guide.md)
- [`docs/playbook-quality-bar.md`](docs/playbook-quality-bar.md)
- [`docs/skill-review-checklist.md`](docs/skill-review-checklist.md)
- [`docs/specialist-authoring-guide.md`](docs/specialist-authoring-guide.md)
