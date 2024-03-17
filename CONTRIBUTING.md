# Contributing to prompit

We love your input! We want to make contributing to this project as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features

## We Develop with Github

We use github to host code, to track issues and feature requests, as well as accept pull requests.

## We Use Github Flow, So All Code Changes Happen Through Pull Requests

Pull requests are the best way to propose changes to the codebase. We actively welcome your pull requests:

1. Fork the repo and create your branch from `main`.
2. If you've added code that should be tested, add tests. You can refer to our example tests in the `tests/` directory.
3. If you've changed APIs, update the documentation.
4. Ensure the test suite passes. You can do this by running `python -m pytest --cov=src` in your terminal.
5. Make sure your code lints. We use `pre-commit` for linting. After installing `pre-commit` using pip, run `pre-commit install` to set up the git hooks on your local machine.
6. Issue that pull request!

## Continuous Integration (CI)

We use a Continuous Integration pipeline to run `pre-commit` on every pull request. This ensures that all code that gets merged into the main branch is properly formatted and passes all the checks. If the checks fail, the pull request cannot be merged until the issues are fixed.

## Development Dependencies

Some packages are needed only for development and not at runtime. These include `pre-commit`, `pytest`, etc. To install these packages, run `pip install -r requirements-dev.txt`.

## Any contributions you make will be under the MIT Software License

In short, when you submit code changes, your submissions are understood to be under the same MIT License that covers the project. Feel free to contact the maintainers if that's a concern.

## Report bugs using Github's issues

We use GitHub issues to track public bugs. Report a bug by opening a new issue; it's that easy!

## Write bug reports with detail, background, and sample code

Great Bug Reports tend to have:

- A quick summary and/or background
- Steps to reproduce
  - Be specific!
  - Give sample code if you can.
- What you expected would happen
- What actually happens

## Use a Consistent Coding Style

We recommend using PEP8 as the coding style guide.

## License

By contributing, you agree that your contributions will be licensed under its MIT License.
