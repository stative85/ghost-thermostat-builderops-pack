# Ghost Thermostat BuilderOps Pack

An operations-first toolkit for designing, documenting, and running Ghost Thermostat build workflows with repeatable standards.

## What This Repository Is For

- Define a clean, versioned operating model for BuilderOps work.
- Standardize delivery artifacts (SOPs, runbooks, templates, release notes).
- Reduce ad-hoc execution by turning process knowledge into reusable assets.

## Scope

This repository is intentionally documentation-first. It is built to support:

- Project planning and execution checklists
- Installation and commissioning runbooks
- Maintenance and incident response playbooks
- Governance, change control, and release process

## Repository Structure

- `docs/` - Core operational documentation and playbooks
- `.github/` - GitHub issue and pull request templates
- `CHANGELOG.md` - Human-readable release history
- `CONTRIBUTING.md` - Contribution workflow and quality bar
- `SECURITY.md` - Security reporting and response expectations

## Quick Start

1. Read `docs/operations/runbook.md`.
2. Review `docs/standards/document-style-guide.md`.
3. Review `docs/strategy/unique-design-claim-and-validation-plan.md`.
4. Open an issue using one of the templates in `.github/ISSUE_TEMPLATE/`.
5. Submit changes through pull requests using the PR template.

## Working Model

- Keep changes small and reviewable.
- Tie each change to an issue or a clear operational need.
- Update docs and changelog in the same pull request.
- Prefer explicit procedures over tribal knowledge.

## Release Process

- Use semantic version tags (`vMAJOR.MINOR.PATCH`).
- Capture notable updates in `CHANGELOG.md`.
- Treat any operationally breaking documentation change as a major release.

## License

This project is released under the MIT License. See `LICENSE`.
