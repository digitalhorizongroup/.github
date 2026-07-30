# Contributing to Digital Horizon Group

Thank you for contributing. These guidelines apply to public Digital Horizon Group repositories unless a project provides more specific instructions.

## Before you start

1. Read the project README and open issues.
2. Confirm that the project is active and accepts contributions.
3. Use an existing issue or open a new one for substantial changes.
4. Do not include secrets, customer data, private infrastructure details, or generated files.

For questions and early discussion, use [Discord](https://discord.gg/fjqzSYCETC).

## Set up the project

Follow the installation and configuration instructions in the project README. If the instructions do not work, open a documentation issue before making unrelated changes.

Never use production credentials for local development. Use placeholders or the provided example configuration.

## Create a branch

Create a focused branch from the default branch:

```bash
git switch main
git pull --ff-only
git switch -c fix/short-description
```

Recommended prefixes:

- `fix/` for bug fixes;
- `feature/` for new functionality;
- `docs/` for documentation;
- `chore/` for maintenance.

## Make changes

- Keep each change focused on one problem.
- Match the existing project style.
- Update documentation when behavior changes.
- Add or update tests when the project has a test suite.
- Do not reformat unrelated files.

Write concise commit messages in the imperative form:

```text
Fix Telegram session path handling
Add installation notes for Linux
```

## Run checks

Run the checks documented by the project. At minimum, verify that:

- the project starts or builds;
- relevant tests pass;
- changed documentation links work;
- no credentials or generated artifacts are staged.

Include the checks you ran in the pull request.

## Open a pull request

Before opening a pull request:

1. Rebase or update your branch from the current default branch.
2. Review the full diff.
3. Complete the pull request template.
4. Link the related issue when one exists.
5. Explain what changed, why, and how it was verified.

Maintainers may request changes or close contributions that are out of scope, unsafe, undocumented, or inconsistent with the project direction.

## New repositories

Proposals for new organization repositories must follow the [New Repository Policy](REPOSITORY_POLICY.md). Do not create public repositories containing unfinished client work, credentials, or code without approved usage terms.
