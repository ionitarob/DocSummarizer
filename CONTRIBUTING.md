# Contributing to DocSummarizer-Student

Thank you for your interest in contributing! This guide will help you get started.

## How to Contribute

1. **Fork the repository** and clone your fork:
   ```bash
   git clone https://github.com/your-username/DocSummarizer-Student.git
   cd DocSummarizer-Student
   ```
2. **Create a new branch** for your feature or bugfix:
   ```bash
   git checkout -b feature/short-description
   ```
3. **Install dependencies** and set up the environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\\Scripts\\activate
   pip install -r requirements.txt
   ```
4. **Make your changes** in the appropriate module under `src/`.
5. **Write tests** for your changes and ensure existing tests pass:
   ```bash
   pytest --maxfail=1 --disable-warnings -q
   ```
6. **Lint your code** (PEP8 style):
   ```bash
   flake8 src/ tests/
   ```
7. **Commit your changes** with a clear message:
   ```bash
   git add .
   git commit -m "Short, descriptive commit message"
   ```
8. **Push to your fork** and create a Pull Request (PR) against `main`:
   ```bash
   git push origin feature/short-description
   ```
9. In your PR description, include:
   - A brief overview of the change.
   - Any relevant issue numbers (e.g., `Closes #12`).
   - Screenshots or logs if applicable.

## Code Style Guidelines

- Follow **PEP 8** for Python code.
- Use **Black** for code formatting:
  ```bash
  black .
  ```
- Keep lines under 88 characters.
- Write meaningful function and variable names.

## Testing

- Add tests under the `tests/` directory.
- Use **pytest** as the test runner.
- Aim for high coverage on new code.

## Issue Reporting

If you encounter a bug or have a feature request, please:
1. Check existing issues to avoid duplicates.
2. Open a new issue with:
   - A clear title.
   - Steps to reproduce the bug or a description of the feature.
   - Expected vs. actual behavior.

## License and Code of Conduct

By contributing to this project, you agree that your contributions will be licensed under the MIT License. Please note that this project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold its standards.

## Contact

For any questions, reach out to the maintainers via GitHub Discussions or open an issue.

---

Thank you for helping make DocSummarizer-Student better!

