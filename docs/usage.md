# Usage

## Quickstart

The "Hyperfast Template" is designed to help you create and manage your projects efficiently. There are two ways to use this project:

1. Create a new project on your local machine using Copier.
2. Inject the Hyperfast Template into an existing project.

### I. Create a New Project with Copier

1. Install Copier using the following command:
   ```bash
   pipx install copier
   ```
2. To create a new project, run:
   ```bash
   copier gh:entelecheia/hyperfast-template path/to/destination
   ```
3. Start working on your new project!

### II. Inject the Template into an Existing Project

1. Install Copier if you haven't already:
   ```bash
   pipx install copier
   ```
2. Navigate to the root of your existing project, then run:
   ```bash
   copier gh:entelecheia/hyperfast-template .
   ```
3. Continue working on your project with the added benefits of the Hyperfast Template.

## Features

- [x] Hyperfast rendering of the template into a new project using [Copier]
- [x] Project management with [Make]
- [x] Support for [Conventional Commits] and [Semantic Versioning]
- [x] Automated changelog with [semantic release]
- [x] Automated semantic versioning with [semantic release]
- [x] Automated labeling for pull requests based on [Conventional Commits] using [Conventional Release Labels]
- [x] Continuous integration with [GitHub Actions]
- [x] Automated dependency updates with [Dependabot]
- [x] Documentation using [MkDocs] and [Read the Docs]
- [x] Consistent coding styles across different text editors with [EditorConfig] and its configuration file `.editorconfig`
- [x] Enforced coding standards and best practices for JavaScript using [ESLint]
- [x] Consistent code style using [Prettier] and its configuration file `.prettierrc`
- [x] Ensured code quality with [pre-commit] and its configuration file `.pre-commit-config.yaml`
- [x] Simplified Git hooks management with [Husky]
- [x] Assisted commit message creation with [Commitizen] for standardized commit messages

[conventional commits]: https://conventionalcommits.org
[conventional release labels]: https://github.com/marketplace/actions/conventional-release-labels
[copier]: https://copier.readthedocs.io
[dependabot]: https://dependabot.com/
[github actions]: https://github.com/features/actions
[make]: https://www.gnu.org/software/make/
[mkdocs]: https://www.mkdocs.org
[poetry]: https://python-poetry.org/
[pre-commit]: https://pre-commit.com/
[prettier]: https://prettier.io/
[semantic release]: https://semantic-release.gitbook.io/semantic-release/
[read the docs]: https://readthedocs.org/
[safety]: https://github.com/pyupio/safety
[semantic versioning]: https://semver.org
[editorconfig]: https://editorconfig.org/
[eslint]: https://eslint.org/
[husky]: https://typicode.github.io/husky
[commitizen]: https://github.com/commitizen/cz-cli

## Semantic Release

### Commit Message Format

**Semantic-release** relies on commit messages to determine the impact of changes in the codebase on users. By adhering to standardized commit message conventions, **semantic-release** can automatically calculate the next [semantic version](https://semver.org) number, generate a changelog, and publish the release.

Tools such as [commitizen](https://github.com/commitizen/cz-cli) or [commitlint](https://github.com/conventional-changelog/commitlint) can assist contributors in maintaining valid commit messages.

The table below demonstrates how different commit messages result in specific release types when `semantic-release` runs (using the default configuration):

| Commit message                                                                                                                                                                                   | Release type                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| `fix(pencil): stop graphite breaking when too much pressure applied`                                                                                                                             | Fix Release                                                                                           |
| `feat(pencil): add 'graphiteWidth' option`                                                                                                                                                       | Feature Release                                                                                       |
| `perf(pencil): remove graphiteWidth option`<br><br>`BREAKING CHANGE: The graphiteWidth option has been removed.`<br>`The default graphite width of 10mm is always used for performance reasons.` | Breaking Release <br /> (Note that the `BREAKING CHANGE: ` token must be in the footer of the commit) |

### Automation with CI

**Semantic-release** is designed to run on a Continuous Integration (CI) environment after every successful build on the release branch. This approach ensures that no human intervention is required during the release process, making releases objective and emotionless.

### Triggering a Release

Whenever a new commit is added to one of the release branches (e.g., `main`, `next`, or `beta`) through `git push`, merging a pull request, or merging from another branch, a CI build is triggered. This build executes the `semantic-release` command, initiating a release if there are any changes to the codebase that affect the package's functionality since the last release.
