# New Repository Policy

This policy defines the minimum requirements for repositories created under the Digital Horizon Group GitHub organization.

## Before creating a repository

Create a repository only when it has a clear owner, purpose, and maintenance plan. Before creation, confirm that the work does not belong in an existing repository.

Every new repository must have:

- a short purpose statement;
- a responsible maintainer;
- an intended visibility level;
- a known audience;
- a decision about whether the project is experimental, active, maintained, or internal.

Do not create empty repositories for ideas that have no implementation plan.

## Repository naming

Repository names must be:

- lowercase;
- short and descriptive;
- separated with hyphens;
- related to the actual project purpose.

Avoid:

- underscores;
- unexplained abbreviations;
- random numbers;
- names containing `test`, `new`, `final`, `latest`, or personal usernames.

Examples:

- `digital-horizon-website`
- `telegram-chat-parser`
- `voip-monitoring`
- `devops-toolkit`

The special `.github` repository is exempt from this naming convention.

## Visibility

Use `private` by default for internal, client, infrastructure, credential-related, or unfinished work.

Use `public` only when:

- the content is safe to publish;
- repository history has been checked for secrets and personal data;
- the project has a clear README;
- the license or usage terms have been approved;
- the project provides value to an external audience.

Changing a repository from private to public requires maintainer review.

## Required metadata

Every public repository must have:

- a one-sentence description;
- the official website when relevant: `https://digitalhorizon.group`;
- approximately 5–12 accurate GitHub topics;
- a custom social preview for primary projects;
- the correct project status.

Do not add unrelated popular topics for search visibility.

## Required files

Before a repository is presented as an active public project, it must contain:

- `README.md`;
- `.gitignore` appropriate for its technology;
- a configuration example when configuration is required;
- contribution and security guidance, inherited from `.github` or defined locally;
- `LICENSE` or explicit usage terms approved by the owner.

Add these files when relevant:

- `CHANGELOG.md`;
- `CODEOWNERS`;
- issue templates;
- pull request template;
- architecture and deployment documentation.

## README requirements

The primary README language is English. A short Russian or Ukrainian section may follow when useful.

The opening must state:

- what the project does;
- its current status;
- its primary technology;
- supported platforms or environments when relevant.

Document only verified features and technologies. Include working installation, configuration, and usage instructions. Never place real credentials, tokens, passwords, private endpoints, or customer data in examples.

## Licensing

Do not select a license automatically for existing code.

The owner must approve one of the following approaches before public release:

- MIT;
- Apache-2.0;
- GPL-3.0;
- proprietary usage terms.

A repository without an approved open-source license must not be described as Open Source.

## Security and secrets

Never commit:

- API keys, tokens, passwords, or private keys;
- `.env` files containing real values;
- session files or authentication cookies;
- production databases, backups, or logs with personal data;
- customer information or private infrastructure details.

Provide `.env.example` or another configuration template with placeholder values. If a secret is committed, rotate it immediately and remove it from Git history where required.

Security vulnerabilities must be reported privately according to `SECURITY.md`, not through a public issue.

## Branches and changes

Use `main` as the default branch.

For shared or production projects:

- make changes in focused branches;
- use descriptive commit messages;
- open a pull request;
- require relevant checks before merge;
- avoid force-pushing protected branches;
- keep unrelated changes in separate pull requests.

Direct pushes to `main` should be limited to repository initialization and explicitly approved maintenance work.

## Automation

Add CI only when it performs a real check, such as:

- tests;
- syntax or type checks;
- linting;
- build validation;
- dependency or security checks.

Do not create workflows only to generate activity. Pin GitHub Actions to trusted versions and grant the minimum required permissions.

## Releases and maintenance

Create releases only for usable project milestones. Use semantic versioning when the project publishes versions.

Each active repository must have a maintainer responsible for:

- reviewing issues and pull requests;
- keeping setup instructions accurate;
- updating dependencies safely;
- documenting breaking changes;
- archiving the repository when it is no longer maintained.

Archive repositories that are abandoned, replaced, or no longer safe to use. Add a clear notice and replacement link before archiving when possible.

## Review checklist

Before publishing or promoting a repository, confirm:

- [ ] The name follows the naming convention.
- [ ] The description clearly explains the project.
- [ ] The README matches the actual code.
- [ ] Installation and usage instructions work.
- [ ] Topics are accurate.
- [ ] No secrets or personal data are present.
- [ ] The license or usage terms are approved.
- [ ] Community and security guidance is available.
- [ ] The official website and organization links are present.
- [ ] The project status is honest and current.

Questions about this policy can be discussed through [Digital Horizon Group Discord](https://discord.gg/fjqzSYCETC).
