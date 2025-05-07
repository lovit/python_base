# Base

A Python package template using uv for dependency management.

## Installation

```bash
# Clone the repository
git clone https://github.com/lovit/base.git
cd base
```

## Development Setup

This project uses uv for dependency management and pre-commit for code quality. Follow these steps to set up your development environment:

1. Install uv if you haven't already:
```bash
pip install uv
```

2. Create and activate a virtual environment:
```bash
# Create virtual environment
uv venv

# Activate virtual environment
source .venv/bin/activate  # On Unix/macOS
# or
.venv\Scripts\activate  # On Windows
```

3. Install dependencies:
```bash
# Install dependencies with locked versions
uv pip install -r requirements.lock

# Install the package in development mode
uv pip install -e .
```

4. Set up pre-commit:
```bash
# Install pre-commit in the virtual environment
uv pip install pre-commit

# Install pre-commit hooks
pre-commit install
```

## Usage

```python
from base import main

# Your code here
```

## Development Workflow

### Running Code Quality Checks

This project uses pre-commit hooks to maintain code quality. The following checks are automatically run before each commit:

- Code formatting (black)
- Import sorting (isort)
- Linting (ruff)
- Type checking (mypy)
- Basic file checks (pre-commit-hooks)

To manually run all checks:
```bash
pre-commit run --all-files
```

### Continuous Integration

This project uses GitHub Actions to run pre-commit checks on every push and pull request to the main branch. The workflow:

1. Sets up Python 3.12
2. Installs uv and dependencies
3. Runs all pre-commit checks

You can see the status of the checks in the badge at the top of this README.

### Updating Dependencies

To update dependencies and regenerate the lock file:

```bash
# Update requirements.lock with the latest compatible versions
uv pip compile requirements.txt -o requirements.lock

# Install updated dependencies
uv pip install -r requirements.lock
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.
