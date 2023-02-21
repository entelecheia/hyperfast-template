# Hyperfast Template

[![license-image]][license-url]
[![version-image]][release-url]
[![release-date-image]][release-url]
[![conventional-commits-image]][conventional commits]
[![jupyter-book-image]][jupyter book]

<!-- Links: -->
[hyperfast template]: https://github.com/entelecheia/hyperfast-template

[license-image]: https://img.shields.io/github/license/entelecheia/hyperfast-template
[license-url]: https://github.com/entelecheia/hyperfast-template/blob/main/LICENSE
[version-image]: https://img.shields.io/github/v/release/entelecheia/hyperfast-template?sort=semver
[release-date-image]: https://img.shields.io/github/release-date/entelecheia/hyperfast-template
[release-url]: https://github.com/entelecheia/hyperfast-template/releases
[conventional-commits-image]: https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white
[jupyter-book-image]: https://jupyterbook.org/en/stable/_images/badge.svg

[repo-url]: https://github.com/entelecheia/hyperfast-template
[pypi-url]: https://pypi.org/project/hyperfast-template
[docs-url]: https://entelecheia.github.io/hyperfast-template
[changelog]: https://github.com/entelecheia/hyperfast-template/blob/main/CHANGELOG.md
[contributing guidelines]: https://github.com/entelecheia/hyperfast-template/blob/main/CONTRIBUTING.md
<!-- Links: -->

A general template that helps you jump start your project

- Documentation: [https://entelecheia.github.io/hyperfast-template][docs-url]
- GitHub: [https://github.com/entelecheia/hyperfast-template][repo-url]
- PyPI: [https://pypi.org/project/hyperfast-template][pypi-url]

Hyperfast Template is a self-contained template that helps you initialize your project inside the template. It is hyperfast in the sense that the template itself is converted into a project in the blink of an eye. It is also hyperfast in the sense that it helps you jump start your project with the best practices in the dev community.

## Quickstart

There are three ways to use this project:

- Use [Hyperfast Template] to create a new repository
- Use [Copier] to create a project to your local machine directly
- Inject [Hyperfast Template] into an existing project

### I. Use the template

1. Click the `Use this template` button
2. Enter a name for your repository
3. Click `Create repository from template`
4. Clone your new repository to your local machine
5. Initialize your project with `make init-project`
6. Do your work

### II. Use Copier

1. Install Copier with `pipx install copier`
2. Run `copier gh:entelecheia/hyperfast-template path/to/destination`
3. Initialize your project with `make init-git`
4. Do your work

### III. Inject the template

1. Install Copier with `pipx install copier`
2. From the root of your project, run `copier gh:entelecheia/hyperfast-template .`
3. If your project is not a git repository, initialize it with `make init-git`
4. Do your work

## Features


- [x] Automated changelog with [Conventional Commits] and [Python Semantic Release]
- [x] Automated labeling to pull requests based on [Conventional Commits] with [Conventional Release Labels]
- [x] Automated semantic versioning with [Python Semantic Release]
- [x] Continuous integration with [GitHub Actions]
- [x] Documentation with [MkDocs], and [Read the Docs]
- [x] Managing project labels with [GitHub Labeler]
- [x] Managing projects with [Make]
- [x] Packaging and dependency management with [Poetry]
- [x] Hyperfast rendering of the template into a new project with [Copier]
- [x] Support for [Conventional Commits]
- [x] Support for [Semantic Versioning]

The template supports Python 3.7, 3.8, 3.9, and 3.10.

[bandit]: https://github.com/PyCQA/bandit
[black]: https://github.com/psf/black
[click]: https://click.palletsprojects.com/
[codecov]: https://codecov.io/
[conventional commits]: https://conventionalcommits.org
[conventional release labels]: https://github.com/marketplace/actions/conventional-release-labels
[copier]: https://copier.readthedocs.io
[coverage.py]: https://coverage.readthedocs.io/
[dependabot]: https://dependabot.com/
[flake8]: http://flake8.pycqa.org
[github actions]: https://github.com/features/actions
[github labeler]: https://github.com/marketplace/actions/github-labeler
[isort]: https://pycqa.github.io/isort/
[jupyter book]: https://jupyterbook.org
[make]: https://www.gnu.org/software/make/
[mkdocs]: https://www.mkdocs.org
[mkdocstrings]: https://mkdocstrings.github.io
[mypy]: http://mypy-lang.org/
[myst]: https://myst-parser.readthedocs.io/
[nox]: https://nox.thea.codes/
[poetry]: https://python-poetry.org/
[pre-commit]: https://pre-commit.com/
[prettier]: https://prettier.io/
[pypi]: https://pypi.org/
[pytest-cov]: https://pytest-cov.readthedocs.io/
[pytest]: https://docs.pytest.org/en/latest/
[python semantic release]: https://python-semantic-release.readthedocs.io/en/latest/
[pyupgrade]: https://github.com/asottile/pyupgrade
[read the docs]: https://readthedocs.org/
[release drafter]: https://github.com/release-drafter/release-drafter
[safety]: https://github.com/pyupio/safety
[semantic versioning]: https://semver.org
[testpypi]: https://test.pypi.org/
[typeguard]: https://github.com/agronholm/typeguard
[xdoctest]: https://github.com/Erotemic/xdoctest

## Changelog

See the [CHANGELOG] for more information.

## Contributing

Contributions are welcome! Please see the [contributing guidelines] for more information.

## License

This project is released under the [MIT License][license-url].
