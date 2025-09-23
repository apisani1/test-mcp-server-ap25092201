# test-mcp-server-ap25092201

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)

A test MCP (Model Context Protocol) server implementation with media handling and prompt capabilities, designed for testing bootstrap scripts and demonstrating MCP integration patterns.

## Overview

This package provides a complete MCP server implementation that includes:

- **Media Handler**: Image and audio processing capabilities with PyAutoGUI integration
- **Prompt Server**: FastMCP-based server with resource management and prompt handling
- **Prompt Client**: OpenAI client integration for AI interactions
- **Bootstrap Testing**: Designed to test mcp-python-bootstrap project compatibility

## Features

- 🖼️ **Image Processing**: Screenshot capture and image manipulation using PyAutoGUI
- 🎵 **Audio Handling**: Audio resource management and processing
- 🤖 **AI Integration**: OpenAI client for prompt processing and responses
- 🔧 **MCP Protocol**: Full Model Context Protocol implementation using FastMCP
- 📦 **Modular Design**: Clean separation between media handling, server logic, and client operations
- 🚀 **Bootstrap Ready**: Prepared for migration from Poetry to uv for bootstrap compatibility

## Installation

### From PyPI

```bash
pip install test-mcp-server-ap25092201
```

### From GitHub

```bash
pip install git+https://github.com/apisani1/test-mcp-server-ap25092201.git
```

### For Development

```bash
git clone https://github.com/apisani1/test-mcp-server-ap25092201.git
cd test-mcp-server-ap25092201
poetry install
```

## Quick Start

### Basic Usage

```python
from test_mcp_server_ap25092201.prompt_server import mcp

# Initialize the MCP server
server = mcp

# The server provides various resources and prompts
# See the MCP protocol documentation for integration details
```

### Running the MCP Server

```bash
# Using the package directly
python -m test_mcp_server_ap25092201.prompt_server

# Or using make commands for development
make run prompt_server
```

### Media Handling

```python
from test_mcp_server_ap25092201.media_handler import get_image, get_audio

# Capture and process images
image_data = get_image("path/to/image.png")

# Handle audio resources
audio_data = get_audio("path/to/audio.wav")
```

### AI Client Integration

```python
from test_mcp_server_ap25092201.prompt_client import create_client

# Initialize OpenAI client
client = create_client()

# Use with your AI workflows
```

## Development

### Prerequisites

- Python 3.10+
- Poetry for dependency management
- Git for version control

### Setup Development Environment

```bash
# Clone the repository
git clone https://github.com/apisani1/test-mcp-server-ap25092201.git
cd test-mcp-server-ap25092201

# Install dependencies
make install-dev

# Run tests
make test

# Run linting
make lint

# Format code
make format
```

### Available Make Commands

```bash
make install      # Install core dependencies
make install-dev  # Install development dependencies
make test         # Run test suite
make lint         # Run linting checks
make format       # Format code with black/isort
make docs         # Build documentation
make build        # Build distribution packages
make publish-test # Publish to TestPyPI
make publish      # Publish to PyPI
```

## Testing Bootstrap Compatibility

This package is specifically designed to test the mcp-python-bootstrap project:

1. **Current State**: Uses Poetry for dependency management
2. **Future Migration**: Will be migrated to uv for bootstrap script compatibility
3. **Testing Target**: Validates bootstrap scripts can properly handle MCP server packages

## Project Structure

```
src/test_mcp_server_ap25092201/
├── __init__.py           # Package initialization
├── media_handler.py      # Image and audio processing
├── prompt_client.py      # OpenAI client integration
└── prompt_server.py      # Main MCP server implementation
```

## Dependencies

### Core Dependencies
- `mcp[cli]` - Model Context Protocol implementation
- `openai` - OpenAI API client
- `pyautogui` - GUI automation and screenshot capabilities
- `pyscreeze` - Screen capture utilities
- `pillow` - Image processing library

### Development Dependencies
- `pytest` - Testing framework
- `black` - Code formatting
- `flake8` - Linting
- `mypy` - Type checking

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Run tests and linting (`make test lint`)
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Related Projects

- [MCP Masterclass](https://mcp-masterclass.readthedocs.io/) - Documentation and tutorials
- [mcp-python-bootstrap](https://github.com/your-org/mcp-python-bootstrap) - Bootstrap scripts for MCP projects
- [FastMCP](https://github.com/jlowin/fastmcp) - Fast MCP server implementation

## Support

- 📖 [Documentation](https://mcp-masterclass.readthedocs.io/)
- 🐛 [Issue Tracker](https://github.com/apisani1/test-mcp-server-ap25092201/issues)
- 💬 [Discussions](https://github.com/apisani1/test-mcp-server-ap25092201/discussions)

---

**Note**: This is a test package designed for bootstrap validation. For production MCP servers, consider using the patterns demonstrated here as a starting point for your own implementation.