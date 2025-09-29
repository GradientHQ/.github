# GradientHQ Development Standards

This repository provides organization-wide .github standards for GradientHQ:
- Pull Request template
- Issue templates
- Commitlint workflow and rules

Current structure:
- PULL_REQUEST_TEMPLATE.md
- .github/.commitlintrc.json
- .github/workflows/commitlint.yml
- .github/ISSUE_TEMPLATE/ (bug_report.yml, feature_request.yml, config.yml)

Note: Some items currently reside under a nested path `.github/.github/`. We recommend migrating them to the standard top-level paths (`.github/workflows/`, `.github/ISSUE_TEMPLATE/`) for consistent auto-detection.

## Use in other repositories
Add a workflow to reuse commitlint:
```yaml
name: Commitlint
on:
  pull_request:
    types: [opened, edited, synchronize]
  push:

jobs:
  lint:
    uses: GradientHQ/.github/.github/workflows/commitlint.yml@main
```
Behavior:
- PR (squash-merge friendly): validates the PR title
- Push: validates all commits in the pushed range

## PR title convention
Format:
```
type(scope): concise description
```
Examples:
- feat(auth): add login validation
- fix(api): resolve timeout issue
Common types: feat, fix, docs, style, refactor, perf, test, chore

## Issue templates
Org-level Bug/Feature templates appear automatically when creating issues.

## Troubleshooting
- header-trim error (trailing whitespace): remove spaces at the end of the PR title or commit message

## Maintenance
- Changes via Pull Requests
- Affects all repos in GradientHQ—review carefully
