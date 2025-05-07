# Base

A Python package template using uv for dependency management.

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/base.git
cd base

# Install dependencies using uv with locked versions
uv pip install -r requirements.lock

# Install the package in development mode
uv pip install -e .
```

## Usage

```python
from base import main

# Your code here
```

## Development

This project uses uv for dependency management. To set up the development environment:

1. Install uv if you haven't already:
```bash
pip install uv
```

2. Create a virtual environment and install dependencies:
```bash
uv venv
source .venv/bin/activate  # On Unix/macOS
# or
.venv\Scripts\activate  # On Windows

# Install dependencies with locked versions
uv pip install -r requirements.lock
```

3. Set up pre-commit hooks:
```bash
pre-commit install
```

### Updating Dependencies

To update dependencies and regenerate the lock file:

```bash
# Update requirements.lock with the latest compatible versions
uv pip compile requirements.txt -o requirements.lock
```

### Code Quality

This project uses pre-commit hooks to maintain code quality. The following checks are performed before each commit:

- Code formatting (black)
- Import sorting (isort)
- Linting (ruff)
- Type checking (mypy)
- Basic file checks (pre-commit-hooks)

To manually run the checks:
```bash
pre-commit run --all-files
```

## License

This project is licensed under the MIT License - see the LICENSE file for details. 