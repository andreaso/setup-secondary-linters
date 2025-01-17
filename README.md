# setup-secondary-linters

Installs a set of secondary linters.

* [actionlint](https://github.com/rhysd/actionlint)
* [hadolint](https://github.com/hadolint/hadolint)
* [markdownlint](https://github.com/igorshubovych/markdownlint-cli)

## Usage

```yaml
steps:
  # ...
  - name: Setup Secondary Linters
    uses: andreaso/setup-secondary-linters@main

  - name: Lint all GitHub Actions workflows
    run: actionlint

  - name: Lint repository README
    run: markdownlint README.md

  - name: Lint some Dockerfile
    run: hadolint path/to/Dockerfile
```
