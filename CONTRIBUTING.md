# Contributing to Cloudlytic

Thank you for your interest in contributing to Cloudlytic! This document provides guidelines for contributing to the project.

## How to Contribute

### Reporting Issues

- Use the GitHub issue tracker to report bugs
- Describe the issue in detail with steps to reproduce
- Include your environment details (OS, Python version, Power BI version)
- Attach screenshots if applicable

### Suggesting Enhancements

- Open an issue with the "enhancement" label
- Clearly describe the feature and its benefits
- Provide examples or mockups if possible

### Pull Requests

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Make your changes
4. Test your changes thoroughly
5. Commit with clear messages (`git commit -m 'Add feature: description'`)
6. Push to your branch (`git push origin feature/your-feature-name`)
7. Open a Pull Request

## Development Setup

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Copy `config/config.example.json` to `config/config.json`
4. Run tests: `python -m pytest` (if tests are added)

## Code Style

- Follow PEP 8 for Python code
- Use meaningful variable and function names
- Add docstrings to functions and classes
- Comment complex logic

## Testing

- Test your changes with sample data
- Verify Power BI dashboard loads correctly
- Check that all scripts run without errors

## Documentation

- Update README.md if adding new features
- Update relevant documentation in `docs/`
- Add comments to complex code sections

## Questions?

Feel free to open an issue for any questions about contributing.
