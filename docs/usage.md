# Usage

## Quickstart

There are two ways to use this project:

- Use [Copier] to create a project to your local machine directly
- Inject [Hyperfast Template] into an existing project

### I. Use Copier

1. Install Copier
   ```bash
   pipx install copier
   ```
2. Run
   ```bash
   copier gh:entelecheia/hyperfast-template path/to/destination
   ```
3. Do your work

### II. Inject the template

1. Install Copier
   ```bash
   pipx install copier
   ```
2. From the root of your project, run
   ```bash
   copier gh:entelecheia/hyperfast-template .
   ```
3. Do your work

## Features

- [x] Automated changelog with [Conventional Commits] and [Python Semantic Release]
- [x] Automated dependency updates with [Dependabot]
- [x] Automated labeling to pull requests based on [Conventional Commits] with [Conventional Release Labels]
- [x] Automated release notes with [Release Drafter]
- [x] Automated semantic versioning with [Python Semantic Release]
- [x] Continuous integration with [GitHub Actions]
- [x] Documentation with [MkDocs], and [Read the Docs]
- [x] Hyperfast rendering of the template into a new project with [Copier]
- [x] Managing project labels with [GitHub Labeler]
- [x] Managing projects with [Make]
- [x] Packaging and dependency management with [Poetry]
- [x] Support for [Conventional Commits]
- [x] Support for [Semantic Versioning]

The template supports Python 3.7, 3.8, 3.9, and 3.10.

[conventional commits]: https://conventionalcommits.org
[conventional release labels]: https://github.com/marketplace/actions/conventional-release-labels
[copier]: https://copier.readthedocs.io
[dependabot]: https://dependabot.com/
[github actions]: https://github.com/features/actions
[github labeler]: https://github.com/marketplace/actions/github-labeler
[isort]: https://pycqa.github.io/isort/
[make]: https://www.gnu.org/software/make/
[mkdocs]: https://www.mkdocs.org
[myst]: https://myst-parser.readthedocs.io/
[poetry]: https://python-poetry.org/
[pre-commit]: https://pre-commit.com/
[prettier]: https://prettier.io/
[python semantic release]: https://python-semantic-release.readthedocs.io/en/latest/
[read the docs]: https://readthedocs.org/
[release drafter]: https://github.com/release-drafter/release-drafter
[safety]: https://github.com/pyupio/safety
[semantic versioning]: https://semver.org
[xdoctest]: https://github.com/Erotemic/xdoctest

## Semantic Release

### Commit message format

**semantic-release** uses the commit messages to determine the consumer impact of changes in the codebase.
Following formalized conventions for commit messages, **semantic-release** automatically determines the next [semantic version](https://semver.org) number, generates a changelog and publishes the release.

Tools such as [commitizen](https://github.com/commitizen/cz-cli) or [commitlint](https://github.com/conventional-changelog/commitlint) can be used to help contributors and enforce valid commit messages.

The table below shows which commit message gets you which release type when `semantic-release` runs (using the default configuration):

| Commit message                                                                                                                                                                                   | Release type                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| `fix(pencil): stop graphite breaking when too much pressure applied`                                                                                                                             | ~~Patch~~ Fix Release                                                                                           |
| `feat(pencil): add 'graphiteWidth' option`                                                                                                                                                       | ~~Minor~~ Feature Release                                                                                       |
| `perf(pencil): remove graphiteWidth option`<br><br>`BREAKING CHANGE: The graphiteWidth option has been removed.`<br>`The default graphite width of 10mm is always used for performance reasons.` | ~~Major~~ Breaking Release <br /> (Note that the `BREAKING CHANGE: ` token must be in the footer of the commit) |

### Automation with CI

**semantic-release** is meant to be executed on the CI environment after every successful build on the release branch.
This way no human is directly involved in the release process and the releases are guaranteed to be [unromantic and unsentimental](http://sentimentalversioning.org).

### Triggering a release

For each new commit added to one of the release branches (for example: `main`, `next`, `beta`), with `git push` or by merging a pull request or merging from another branch, a CI build is triggered and runs the `semantic-release` command to make a release if there are codebase changes since the last release that affect the package functionalities.
