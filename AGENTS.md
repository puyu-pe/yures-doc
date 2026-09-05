# Agent Instructions

## Python and MkDocs

Before reporting a Python or MkDocs tool as unavailable, check the repository
virtual environment from the repository root. Do not depend on an activated
shell environment.

- Use `.venv/bin/python -m pip ...` for Python package commands.
- Use `.venv/bin/mkdocs build --strict --clean` to validate the documentation.
- If `.venv` exists but dependencies are missing, install them with
  `.venv/bin/python -m pip install -r requirements.txt` and retry the command.
- Only if `.venv` does not exist, create it with `python3 -m venv .venv`, then
  install dependencies with `.venv/bin/python -m pip install -r requirements.txt`.
