# Python Project Template (`uv` + Ruff + Pyrefly)

[![CI (Ruff & Pyrefly)](https://github.com)](https://github.com)
[![Ruff](https://shields.io)](https://github.com)
[![uv](https://shields.io)](https://github.com)

Modern Python project template pre-configured with **`uv`** for dependency management, **Ruff** for linting and formatting, **Pyrefly** for static type checking, **`pre-commit`** hooks, and **GitHub Actions** CI.

## Features

- **Package & Environment Management:** Fast dependency resolution and lockfile management via [`uv`](https://astral.sh).
- **Linting & Formatting:** Configured via [`Ruff`](https://astral.sh) (`E`, `F`, `I`, and `UP` rules, 120-char line length).
- **Static Type Checking:** Powered by [`Pyrefly`](https://pyrefly.org).
- **Automated Quality Gates:** Local `pre-commit` hooks and remote GitHub Actions CI running on every pull request and push to `main`.

## Getting Started

### 1. Create a repository from this template
Click the **"Use this template"** button on GitHub to create your new repository, then clone it locally:

```bash
git clone https://github.com
cd novo-projeto
```

### 2. Install dependencies
Sync the virtual environment and install development tools (including Pyrefly):

```bash
uv sync
```

### 3. Activate `pre-commit` hooks
*(Skip this step if you already have `init.templateDir` configured globally in Git.)*

```bash
pre-commit install
```

## Common Commands

| Task | Command |
| :--- | :--- |
| Add a runtime dependency | `uv add <package>` |
| Add a dev dependency | `uv add --dev <package>` |
| Run a Python script | `uv run python main.py` |
| Run Ruff linter manually | `uvx ruff check --fix` |
| Run Ruff formatter manually | `uvx ruff format` |
| Run Pyrefly type checker | `uv run pyrefly check` |
| Run all pre-commit hooks | `pre-commit run --all-files` |
