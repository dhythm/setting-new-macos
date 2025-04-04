# Python

## インストール

```sh
pyenv install --list
pyenv install <version>
pyenv versions

pyenv global <version>
pyenv local <version>
pyenv shell <version>
```

## パッケージ管理ツール

### Poetry

https://github.com/python-poetry/poetry

#### インストール

```sh
curl -sSL https://install.python-poetry.org | python3 -
# or
pipx install poetry

mkdir $ZSH_CUSTOM/plugins/poetry
poetry completions zsh > $ZSH_CUSTOM/plugins/poetry/_poetry
```

#### 使い方

```sh
poetry config virtualenvs.in-project true
```

```sh
poetry new <project>

poetry install
poetry add <package>
poetry run python <program>
```

### uv

#### インストール

https://github.com/astral-sh/uv

```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
uv self update
```

#### 使い方

```sh
uv init <project>

uv sync
uv add <package>
uv add --dev <package>
uv remove <package>
uv run <program>
```
