# setup-secondary-linters

Installs a set of secondary linters.

* [hadolint](https://github.com/hadolint/hadolint)
* [markdownlint](https://github.com/igorshubovych/markdownlint-cli)
* [zizmor](https://github.com/zizmorcore/zizmor)

## Usage

```yaml
steps:
  # ...
  - name: Setup Secondary Linters
    uses: andreaso/setup-secondary-linters@62a905725ef427318105bead9c74f9ec4e5a779a # v0.2

  - name: Analyze all GitHub Actions workflows
    run: zizmor .
    env:
      GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}

  - name: Lint repository README
    run: markdownlint README.md

  - name: Lint some Dockerfile
    run: hadolint path/to/Dockerfile
```
