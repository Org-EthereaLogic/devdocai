# DevDocAI

A comprehensive AI-powered documentation analysis and enhancement tool designed for developers who want to improve their documentation quality systematically.

## Overview

DevDocAI provides intelligent analysis of documentation files, offering quality scores across multiple dimensions including readability, structure, security, and technical completeness. Built with privacy-first principles and local LLM integration capabilities.

## Key Features

- **Multi-dimensional Quality Analysis**: Performance, security, completeness, and MIAIR entropy-optimized scoring
- **Zero-Configuration First Experience**: Works out of the box with sensible defaults
- **Privacy-First Design**: Complete air-gapped operation capability with local LLM support
- **Batch Processing**: Efficient analysis of entire documentation sets
- **CLI and API Interfaces**: Flexible integration options for any workflow
- **Performance Optimized**: Sub-second analysis for files up to 50KB

## Documentation

- [User Stories & Requirements](docs/devdocai-user-stories.md) - Complete feature specifications and acceptance criteria
- [Build Methodology](docs/build-methodology.md) - The Unified Development Excellence Framework (UDEF) used for this project
- [API Documentation](docs/api/) - REST API reference and examples
- [CLI Reference](docs/cli/) - Command-line interface documentation

## Quick Start

```bash
# Analyze a single documentation file
devdocai analyze README.md

# Batch process documentation directory
devdocai batch docs/

# Get help on available commands
devdocai --help
```

## Development

This project follows the [Unified Development Excellence Framework (UDEF)](docs/build-methodology.md), a comprehensive methodology for predictable, high-quality software delivery.

### Prerequisites

- Docker and Docker Compose
- Python 3.11+ (for local development)
- Git

### Local Development Setup

```bash
# Clone the repository
git clone https://github.com/Org-EthereaLogic/DevDocAI.git
cd DevDocAI

# Build development environment
docker build -t devdocai:test --target test .

# Run tests
docker run --rm -v $(pwd):/app devdocai:test pytest

# Run with coverage
docker run --rm -v $(pwd):/app devdocai:test \
  pytest --cov=src --cov-branch --cov-report=html
```

## Project Status

**Phase**: Documentation and Specification Complete  
**Version**: 3.0 (in development)  
**License**: [MIT](LICENSE)

## Contributing

We welcome contributions! Please read our contributing guidelines and ensure all code follows our quality standards:

- 95% test coverage minimum
- All pre-commit checks passing
- Documentation updated with changes
- Follows UDEF methodology principles

## Support

For questions, issues, or feature requests, please use the GitHub issue tracker.

## Architecture

Built following hexagonal architecture principles with:

- **Core Domain**: Documentation analysis and enhancement logic
- **Application Services**: CLI and API interfaces  
- **Infrastructure**: Local LLM integration, file system operations
- **Quality Assurance**: Comprehensive test suite with performance benchmarks

---

*DevDocAI v3.0 - Empowering developers with private, powerful documentation enhancement*