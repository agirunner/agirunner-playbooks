# Agirunner Playbooks

Community playbooks, specialists, and skills for Agirunner.

The Agirunner Playbooks repository is the public source of truth for
importable catalog content. The platform imports one playbook at a time
from this repository, resolves the referenced specialists and skills,
and creates normal tenant-local copies inside the dashboard and
platform.

## Documentation

Product and operator documentation lives at
[`docs.agirunner.dev`](https://docs.agirunner.dev).

Useful entry points:

- [Getting Started](https://docs.agirunner.dev/getting-started/introduction/)
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
- One playbook at a time: operators choose a single playbook to import.
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
2. Pick a playbook by category, stability, and summary.
3. Read that playbook folder:
   - `playbook.yaml`
   - `README.md`
4. Follow its referenced specialists and skills through:
   - [`catalog/specialists.yaml`](catalog/specialists.yaml)
   - [`catalog/skills.yaml`](catalog/skills.yaml)

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
- workflow semantics authored in prose inside
  `definition.process_instructions`

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
