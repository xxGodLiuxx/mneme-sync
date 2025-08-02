# Contributing to Mneme

Thank you for your interest in contributing to Mneme! This document provides guidelines for contributions.

## How to Contribute

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

## Development Setup

1. Clone your fork
2. Install Python 3.7+
3. Test the setup script in a safe environment

## Code Style

- Follow PEP 8 for Python code
- Use meaningful variable names
- Add comments for complex logic
- Keep functions focused and small

## Testing

Before submitting:
- Test on Windows (primary platform)
- Verify Dropbox detection works
- Ensure configuration is properly loaded
- Check that generated batch files work

## Adding Features

When adding new features:
- Maintain backward compatibility
- Update documentation
- Add configuration options if needed
- Consider privacy implications

## Reporting Issues

When reporting issues, please include:
- Python version
- Operating system
- Dropbox installation path
- Error messages (if any)
- Steps to reproduce

## Privacy Guidelines

- Never hardcode personal information
- Use environment variables for sensitive data
- Make all paths configurable
- Document any data collection

## Questions?

Feel free to open an issue for any questions about contributing.