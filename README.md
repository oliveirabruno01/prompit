﻿# prompit [![Common Changelog](https://common-changelog.org/badge.svg)](CHANGELOG.md) ![GitHub release (latest by date)](https://img.shields.io/github/v/release/oliveirabruno01/prompit)

`prompit` is a Python package and a Command Line Interface (CLI) tool designed to transform repositories, directories, and files into promptable texts for use with large language models. It's an invaluable tool for quickly understanding the structure of a new project and preparing it for interaction with AI models.

## Features

- List all files in your project, considering .gitignore files.
- Print the directory structure of your project.
- Transform your repository into a promptable text.

## Installation

To install `prompit` from source, clone this repository and run the following command:

```shell
cd prompit
python -m pip install -e .
```

Alternatively you can install `prompit` with `pip install prompit`

## Usage

### As a CLI tool

You can use `prompit` to list all non-ignored files in your project:

```shell
prompit --list
```

To print the directory structure:

```shell
prompit --structure
```

To print the current directory or repo as a prompt:

```shell
prompit
```

This will promptfy your repo ignoring files under your .gitignore file. You can also append an instruction message on the prompt:

```shell
prompit --message "Your instruction here"
```

### As a Python module

You can also use `prompit` as a Python module in your scripts. Here's an example:

```python
from prompit import list_files, get_promptified_repo, get_repo_structure

# List all non-ignored files in the current directory
filepaths = list_files()

# Get the repository's structure, excluding all .svg files
structure = get_repo_structure(ignore_files="*.svg")

# Print the promptified repository
print(get_promptified_repo())
```

## Examples

Here are some advanced examples of how you can use `prompit`:

- To get a single file:

```shell
prompit -i * -a single_file.py
```

Note that the exact behavior may depend on your environment. `*` it will work on Windows but on unix-like systems it will probably fail. The exact reason can be explained by your favorite LLM.

> In Unix-like systems, wildcard characters like `*` are expanded by the shell before being passed to commands, which can lead to unexpected behavior. However, in Windows Command Prompt or PowerShell, these characters are passed as-is to the command. To ensure consistent behavior across different systems, you can prevent the shell from expanding the wildcard by quoting it, like so: `prompit -i '*'`. This allows the command itself to handle the wildcard expansion.

- To ignore a specific file and print the structure to the clipboard. This example uses Windows's clip.exe:

```shell
prompit -i src/languages.json -s | clip
```

- For Node.js projects, you might want to ignore `package-lock.json`:

```shell
prompit -i package-lock.json
```

Note: `.gitignore` and `.git` specs are the only ones automatically ignored.

## Contributing

We welcome contributions! Please see our [CONTRIBUTING.md](#CONTRIBUTING.md) for details on how to contribute to this project.
