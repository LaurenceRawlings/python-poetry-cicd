# Python Poetry CI/CD

Python Poetry package with basic CI/CD using GitHub actions

## Usage

- Make new repo with this template
- Add `PERSONAL_ACCESS_TOKEN` and `PYPI_TOKEN` secrets
- Clone your new repo
- [optional] Install recommended VScode extensions
- Install dependencies and update python interpreter path

```bash
poetry install
poetry run pre-commit install
poetry env info
```

- Create a new branch to start development

```bash
git branch <branch_name>
git checkout <branch_name>
```

- Replace all occurances of `application` with the name of your package
  - `pyproject.toml`
  - `.github/workflows/deploy.yml`
  - `application/__main__py`
  - `application` - directory
  - (tip) In VScode use `Ctrl+Shift+F`
- Check the tests are passing before commiting

```bash
poetry run pytest
```

- Commit your changes usig the [conventional commits](https://www.conventionalcommits.org/) format
  - (tip) use the VScode [Conventional Commits](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits) extension to help

```bash
git add .
git commit
```

- Push your changes to GitHub

```bash
git push
```

- Go to your newly created branch on GitHub and create pull request
- Wait for checks to pass from the CI workflow
- Merge pull request after all the checks have passed
- Now back on the `main` branch more workflows should start
- Wait for all the workflows to finish and go to `/releases`
- Review the release draft and publish when ready
