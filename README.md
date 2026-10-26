# service-config

Python configuration management library for microservice deployments.

Provides a unified interface for loading, validating, and managing service
configuration across development, staging, and production environments.

## Features

- Environment-aware config loading (`dev` / `staging` / `prod`)
- Schema validation via `pydantic`
- Secret resolution from environment variables or Vault
- Hot-reload support for long-running services

## Installation

```bash
pip install service-config
```

## Usage

```python
from service_config import load_config

config = load_config("api_service", env="prod")
print(config.api_url)
```

## Configuration Format

```python
config = {
    "api_url": "https://api.example.com",
    "timeout": 30,
    "retry_count": 3,
    "version": "1.0.0",
}
```

## Contributing

Open a PR against `main`. All changes require passing CI and a code review.
