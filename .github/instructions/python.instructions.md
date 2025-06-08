---
applyTo: "**/*.py"
---
# Python Coding Standards for Copilot

- Follow PEP 8 style guide for code formatting.
- Use type hints and static type checking (mypy, Pyright).
- Prefer pathlib for file paths and f-strings for formatting.
- Use virtual environments for dependencies.
- Organize code into packages and modules.
- Write docstrings for all public functions, classes, and modules.
- Handle exceptions explicitly and log errors with context.
- Use Black for code formatting and Ruff or Flake8 for linting.
- Write unit tests with pytest or unittest.
- Avoid global variables and side effects in modules.
- Never commit secrets or credentials to the repository.
- Validate and sanitize all user input.
- Use environment variables for sensitive configuration.
- Keep dependencies up to date and review for vulnerabilities.
- Write tests for critical paths and edge cases.
- Document all setup, build, and deployment steps in README.md.
