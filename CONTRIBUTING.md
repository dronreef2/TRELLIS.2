# Contributing to TRELLIS.2

Thank you for your interest in contributing to TRELLIS.2! This document provides guidelines for contributing to the project.

## Getting Started

1. Fork the repository
2. Clone your fork with submodules: `git clone --recursive https://github.com/YOUR_USERNAME/TRELLIS.2.git`
3. Set up the development environment following the [Installation](README.md#installation) instructions

## Development Guidelines

### Code Quality

Before submitting a pull request, ensure your code:

1. **Passes syntax checks**: Run `python -m py_compile` on your Python files
   ```bash
   python -m py_compile your_file.py
   ```

2. **Passes linting**: Use Ruff for linting
   ```bash
   pip install ruff
   ruff check .
   ```

3. **Follows code formatting**: We use Black for code formatting (informational)
   ```bash
   pip install black
   black --check .
   ```

4. **Has no security issues**: Run Bandit security checks
   ```bash
   pip install bandit
   bandit -r trellis2
   ```

### Continuous Integration

All pull requests automatically run through our CI pipeline which:
- Tests code on Python 3.8, 3.9, 3.10, and 3.11
- Runs linting checks with Ruff
- Validates Python syntax
- Performs security scanning with Bandit
- Checks code formatting with Black

You can view the CI status in the pull request or in the [Actions](https://github.com/dronreef2/TRELLIS.2/actions) tab.

### Making Changes

1. Create a new branch for your feature or bugfix
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes following the existing code style
   - Keep changes minimal and focused
   - Maintain consistency with existing code patterns
   - Add comments where necessary to explain complex logic

3. Test your changes locally
   - Ensure all existing functionality still works
   - Test new features thoroughly

4. Commit your changes with clear, descriptive messages
   ```bash
   git commit -m "Add feature X to improve Y"
   ```

5. Push to your fork and submit a pull request
   ```bash
   git push origin feature/your-feature-name
   ```

## Pull Request Process

1. Ensure your PR description clearly describes the problem and solution
2. Include any relevant issue numbers
3. Update documentation if you're changing functionality
4. Ensure all CI checks pass
5. Wait for maintainer review

## Code Style

- Follow PEP 8 guidelines for Python code
- Use meaningful variable and function names
- Keep functions focused and concise
- Add docstrings for public functions and classes

## Questions?

If you have questions about contributing, feel free to open an issue for discussion.

## License

By contributing to TRELLIS.2, you agree that your contributions will be licensed under the MIT License.
