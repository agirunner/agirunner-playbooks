# agirunner-playbooks

Community playbooks, specialists, and skills for Agirunner.

This repository is the public source of truth for importable community
catalog content. The dashboard imports one playbook at a time from this
repository, then creates normal tenant-local copies of the playbook,
specialists, and skills inside the platform.

## Principles

- Content only: YAML and Markdown only.
- One playbook at a time: operators pick a single playbook to import.
- Local ownership after import: imported artifacts become normal local copies.
- Prose-driven workflows: playbook `process_instructions` is the primary
  execution contract.
- Storage agnostic: playbooks support `git`, `host_directory`, and
  `artifact` workspaces.
- Shared reuse: specialists attach reviewed shared skills, and playbooks
  attach shared specialists.

## Repository Layout

```text
catalog/      browse manifests used by the platform import flow
docs/         authoring guidance and review checklists
playbooks/    importable playbook definitions and README docs
schemas/      human-readable schema references
skills/       shared SKILL.md artifacts
specialists/  shared specialist definitions and prompts
```

## Artifact Rules

Skills:
- one `SKILL.md` file per skill
- standard frontmatter only: `name`, `description`

Specialists:
- `specialist.yaml`
- `allowed_tools` may be an explicit list or `all-specialist-tools`

Playbooks:
- `playbook.yaml`
- `README.md`

Category folders exist for repository organization only. The live
product should not expose folder-shaped identities.

## Authoring Bar

Curated playbooks in this repository must be ready to import and use.
They are not templates waiting for operators to finish them later.

Each playbook must author:
- explicit stages and stage goals
- named specialists
- a clear happy path
- at least one unhappy path
- completion rules
- guided-closure language
- storage behavior in prose when it matters

See:
- [`docs/catalog-authoring-guide.md`](docs/catalog-authoring-guide.md)
- [`docs/playbook-quality-bar.md`](docs/playbook-quality-bar.md)
- [`docs/skill-review-checklist.md`](docs/skill-review-checklist.md)
- [`docs/specialist-authoring-guide.md`](docs/specialist-authoring-guide.md)

## Import Model

The platform should browse catalog entries from `catalog/*.yaml`, fetch
the selected playbook package plus its referenced specialists and
skills, preview conflicts, and import tenant-local copies.

## Current Catalog

The curated catalog is organized into:
- engineering
- operations
- research
- compliance
- content

Engineering playbooks may be marked experimental when they rely on
narrow, human-gated SDLC flows such as bug-fix and hotfix.
