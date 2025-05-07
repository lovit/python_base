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

### Updating Dependencies

To update dependencies and regenerate the lock file:

```bash
# Update requirements.lock with the latest compatible versions
uv pip compile requirements.txt -o requirements.lock
```

## License

This project is licensed under the MIT License - see the LICENSE file for details. 