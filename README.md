# Agirunner Playbooks

[![Docs](https://img.shields.io/badge/docs-docs.agirunner.dev-0f766e)](https://docs.agirunner.dev)
[![Agirunner](https://img.shields.io/badge/product-agirunner-111827)](https://github.com/agirunner/agirunner)
[![License](https://img.shields.io/github/license/agirunner/agirunner-playbooks)](./LICENSE)

Community playbooks, specialists, and skills for Agirunner.

The Agirunner Playbooks repository is the public source of truth for
importable catalog content. The platform imports playbooks from this
repository, resolves the referenced specialists and skills, and creates
normal tenant-local copies inside the dashboard and platform.

## Documentation

Product and operator documentation lives at
[`docs.agirunner.dev`](https://docs.agirunner.dev).

Useful entry points:

- [Getting Started](https://docs.agirunner.dev/getting-started/introduction/)
- [Playbooks And Authoring](https://docs.agirunner.dev/dashboard/playbooks-and-authoring/)
- [Platform Overview](https://docs.agirunner.dev/platform/overview/)
- [Dashboard Overview](https://docs.agirunner.dev/dashboard/overview/)
- [Architecture Overview](https://docs.agirunner.dev/architecture/overview/)

For the public product entry point, start with
[`agirunner`](https://github.com/agirunner/agirunner). This repository
is the right place when you want to work on the shared catalog content
itself.

## What This Repository Contains

- 17 shared skills under [`skills/`](skills)
- 15 shared specialists under [`specialists/`](specialists)
- 17 playbooks under [`playbooks/`](playbooks)
- catalog manifests under [`catalog/`](catalog)
- authoring guidance under [`docs/`](docs)
- human-readable schema references under [`schemas/`](schemas)

## Catalog Principles

- Content only: YAML and Markdown only.
- Catalog import: operators choose playbooks to import into their
  tenant-local library.
- Local ownership after import: imported artifacts become normal tenant-
  local copies.
- Prose-driven workflows: `definition.process_instructions` is the
  primary workflow contract.
- Storage-agnostic design: playbooks are written to work with `git`,
  `host_directory`, and `artifact` workspace modes.
- Reusable building blocks: playbooks reference shared specialists, and
  specialists reference shared skills.

## Quick Start

To browse the catalog:

1. Start with [`catalog/playbooks.yaml`](catalog/playbooks.yaml).
2. Pick a playbook by category, author, stability, and summary.
3. Read that playbook folder:
   - `playbook.yaml`
   - `README.md`
4. Follow its referenced specialists and skills through:
   - [`catalog/specialists.yaml`](catalog/specialists.yaml)
   - [`catalog/skills.yaml`](catalog/skills.yaml)

To use the catalog in the product:

1. Start with [`agirunner`](https://github.com/agirunner/agirunner) for
   the full-stack product entry point and local bring-up path.
2. Open the dashboard and go to **Work Design -> Playbooks**.
3. Use **Add Community Playbook** to browse this catalog, inspect the
   playbook README, and import selected playbooks into your tenant.
4. Treat imported artifacts as normal tenant-local copies after import.

## Repository Layout

```text
catalog/      catalog manifests and shared tool profiles
docs/         authoring guidance and review checklists
playbooks/    importable playbook definitions and README docs
schemas/      human-readable schema references
skills/       shared SKILL.md artifacts
specialists/  shared specialist definitions
```

Category folders exist for repository organization only. Category paths
should not become live product identities.

## Artifact Formats

Skills:
- one `SKILL.md` file per skill
- standard frontmatter only: `name`, `description`
- concise by design, usually at or under 100 lines

Specialists:
- one `specialist.yaml` file per specialist
- full `system_prompt` stored inline in YAML
- `allowed_tools` may be an explicit list or
  `all-specialist-tools`

Playbooks:
- one `playbook.yaml` file per playbook
- one `README.md` file per playbook
- required metadata includes `id`, `name`, `author`, `version`,
  `category`, and `stability`
- workflow semantics authored in prose inside
  `definition.process_instructions`

Catalog manifest entries:
- `catalog/playbooks.yaml` is the import-facing index used by the
  dashboard
- each entry should carry the same human-facing identity fields as the
  underlying playbook, including `author`
- manifest metadata should stay aligned with the referenced
  `playbook.yaml`

## Import Model

The dashboard imports catalog content over GitHub and creates normal
tenant-local artifacts in the platform:

- operators can import one playbook, a selected subset, or the full
  filtered set
- referenced specialists and skills are imported alongside the selected
  playbooks
- imported artifacts can be created as new local copies or used to
  override matching local artifacts at import time
- after import, the resulting playbooks, specialists, and skills behave
  like normal local platform content

## Process Instruction Style

Playbook `process_instructions` should read like an execution brief. The
normal authored sections are:

- `Preferred flow`
- `Recovery and exception handling`
- `Completion rules`
- `Guided closure rule`

Those are prose conventions, not separate runtime fields.

## Tool Profiles

Most specialists use the shared tool profile in
[`catalog/tool-profiles.yaml`](catalog/tool-profiles.yaml):

- `all-specialist-tools`

That alias exists so the catalog can stay readable while the platform
still expands to the explicit allowed tool list during import.

## Current Catalog

Stable categories:
- Operations: customer support triage, SOP creation, runbook creation
- Research: research analysis, lead research pipeline, vendor
  evaluation, business case
- Compliance: policy review, contract review
- Content: technical documentation, API documentation, content pipeline

Experimental engineering playbooks:
- bug fix
- hotfix
- code review
- PR guardian
- regression monitor

The engineering set is intentionally narrow. These workflows are meant
for bounded SDLC tasks with explicit review and human judgment, not
broad autonomous feature delivery.

## Authoring Bar

Curated artifacts in this repository must be ready to import and use.
They are not placeholders waiting for an operator to finish them later.

Each playbook must author:
- a stable catalog identity and a visible author
- explicit stages and stage goals
- named specialists
- a preferred flow
- recovery and exception handling
- completion rules
- guided-closure language
- storage behavior in prose when it matters

Use these docs when contributing:
- [`docs/catalog-authoring-guide.md`](docs/catalog-authoring-guide.md)
- [`docs/playbook-quality-bar.md`](docs/playbook-quality-bar.md)
- [`docs/skill-review-checklist.md`](docs/skill-review-checklist.md)
- [`docs/specialist-authoring-guide.md`](docs/specialist-authoring-guide.md)

Before opening a playbook contribution, check that:
- `catalog/playbooks.yaml` and the referenced `playbook.yaml` agree on
  `name`, `author`, `version`, `category`, and `summary` intent
- the README explains when the playbook should and should not be
  imported
- the authored process instructions are strong enough to stand on their
  own after import

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for contribution rules and
artifact-specific guidance.

## Related Repositories

- [agirunner](https://github.com/agirunner/agirunner): top-level
  product entry point, docs, and full-stack framing
- [agirunner-platform](https://github.com/agirunner/agirunner-platform):
  control plane, dashboard, API, and catalog import implementation
- [agirunner-runtime](https://github.com/agirunner/agirunner-runtime):
  execution plane for task execution and tool runtime behavior

## License

This repository is licensed under Apache 2.0. See [`LICENSE`](LICENSE).
