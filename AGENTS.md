# awp-config-github-community — Agent instructions

## Project
- This is the default GitHub community health repository for the aiworkflowpro organization.
- The remote repository is named `.github`; the local four-part directory name is `awp-config-github-community`.
- GitHub serves these default files to every organization repository that does not define its own version.

## Layout
- `README.md`: what this repository is for and where it applies.
- `CODE_OF_CONDUCT.md`: code of conduct.
- `CONTRIBUTING.md`: contribution guide.
- `SECURITY.md`: how to report vulnerabilities.
- `SUPPORT.md`: support channels.
- `.github/ISSUE_TEMPLATE/`: issue templates.
- `.github/PULL_REQUEST_TEMPLATE.md`: pull request checklist.
- `.github/workflows/`: GitHub Actions for this repository.
- `assets/`: images referenced by README and other documents.

## Commands
- This repository has no package manifest and no local build or test commands.
- Verify Markdown references against the actual file paths, one by one.
- Check changes with `git diff --check`.
- Check template changes with `git diff -- .github/`.

## Boundaries
- Default files apply to the whole aiworkflowpro organization.
- Before changing the code of conduct, check README and CODE_OF_CONDUCT.
- Before changing the security contact, check the existing channels in SECURITY.
- Before changing support information, check the existing text in SUPPORT.
- When changing issue templates, keep the YAML format and the purpose of each field.
- When changing the pull request template, keep the existing link to the contribution guide.
- Organization defaults never override a repository's own file of the same name.
- Do not put repository-specific rules into organization defaults.
- Do not change the `.github` remote name convention.

## Verification
- Check every changed Markdown link.
- For YAML, check indentation and fields.
- For templates, read the resulting issue or pull request form.
- Confirm the change really applies to the whole organization.

## Working rules
- Read this repository's `README.md` first (if present); current files and scripts are the source of truth.
- Only change the files the task needs; do not reorder unrelated content.
- Run checks proportionate to the change; when one fails, fix the implementation, not the test result.
- Before committing, run `git diff --check` and `git status --short`.
- Stage only the files you changed; the commit message describes the actual change.
- Do not credit AI tools in commit messages.
- Never commit secrets, tokens, real `.env` files or runtime data.
- For anything touching remotes, deployment or public content, check the existing configuration and project constraints first.

## Pre-commit checklist
- File paths still match the entry points listed in README.
- New references point to real files in this repository or to explicit external addresses.
- Unrelated existing changes in this repository stay untouched.
- The report states the verification commands, environment and any steps not run.

## Where to look
- For more project facts, continue from the relevant README section.
- For concrete actions, follow the current files and scripts in this repository.
- Check external service status live; do not infer it from repository text.
