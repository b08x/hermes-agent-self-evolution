```markdown
# hermes-agent-self-evolution Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns used in the `hermes-agent-self-evolution` Python project. You'll learn about the repository's coding conventions, commit patterns, file organization, and how to write and run tests. This guide is ideal for contributors aiming for consistency and maintainability in this codebase.

## Coding Conventions

### File Naming
- Use **snake_case** for all Python files.
  - Example: `agent_core.py`, `data_utils.py`

### Import Style
- Use **relative imports** within the package.
  - Example:
    ```python
    from .utils import parse_config
    from .models.agent import Agent
    ```

### Export Style
- Use **named exports** (explicitly define what is exported from a module).
  - Example:
    ```python
    __all__ = ["Agent", "parse_config"]
    ```

### Commit Patterns
- Follow **conventional commit** style.
- Use prefixes like `fix` for bug fixes.
  - Example:
    ```
    fix: resolve agent state update bug in agent_core.py
    ```

## Workflows

### Code Contribution
**Trigger:** When you want to add or update code in the repository  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Make your code changes, following the coding conventions.
3. Write or update tests in files matching `*.test.*`.
4. Commit your changes with a conventional commit message (e.g., `fix: ...`).
5. Push your branch and open a pull request.

### Running Tests
**Trigger:** When you want to verify your code changes  
**Command:** `/run-tests`

1. Identify test files (pattern: `*.test.*`).
2. Run tests using your preferred Python test runner (e.g., `pytest`, `unittest`).
   - Example:
     ```bash
     pytest
     ```
3. Ensure all tests pass before merging.

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `agent_core.test.py`).
- The specific test framework is not specified; use standard Python frameworks like `pytest` or `unittest`.
- Place tests close to the code they test or in a dedicated `tests/` directory.
- Example test structure:
  ```python
  # agent_core.test.py
  import unittest
  from .agent_core import Agent

  class TestAgent(unittest.TestCase):
      def test_agent_initialization(self):
          agent = Agent()
          self.assertIsNotNone(agent)
  ```

## Commands
| Command        | Purpose                                    |
|----------------|--------------------------------------------|
| /contribute    | Start the code contribution workflow        |
| /run-tests     | Run all tests in the repository             |
```
