---
title: "Python Tool - Poetry"
date: 2023-02-19T14:01:57-05:00
slug: python-poetry
toc: true
tags: ["Python"]
draft: true
---

## What is Poetry?

**Poetry** is a Python dependency management and packaging tool. Poetry offers a lock file for dependency management which helps pin the exact version of libraries the project needs so the correct library stack is used wherever the project is installed. Poetry has a system requirement of **Python 3.7+**. 

## How is it different from the PIP tool?

Poetry is built on top of another popular Python dependency management tool - **PIP** and extends PIP's feature set. 
- Poetry provides package management using exact versions of the dependent libraries using the `poetry.lock` file mechanism similar to `npm/yarn`. PIP uses the `requirements.txt` file to manage the project's dependencies. If only the higher-level dependencies are maintained in the PIP's `requirements.txt` file, there can be errors during the build process when the lower-level package updates introduce breaking changes.

- Poetry comes with a simple `pyproject.toml` based configuration file replacing PIP equivalent `setup.py`, `requirements.txt`, `setup.cfg`, `MANIFEST.in` and `Pipfile` configuration files. It also helps with generating and publishing standalone packages with the `build` and `publish` easy-to-use commands.

- Poetry creates a virtual environment in `{cache-dir}/virtualenvs` enforcing environment isolation by default which requires an additional step when using PIP as the dependency management tool.

## Poetry - Getting started

Poetry can be installed using the instructions provided [here](https://python-poetry.org/docs/#installation "Poetry installation instructions").

A new project can be created using the command - `poetry new <project_name>`. This command creates a project structure with a `pyproject.toml` configuration file. This configuration file stores the project's metadata information, library dependencies, and build system information.

Poetry can be added to the existing project using the `poetry init` command.

## Poetry commands

- Run `poetry install` command to install existing project dependencies from the project folder. This will create the `poetry.lock` file containing exact library dependencies and should be checked into version control for replicating the project environment across various tiers.

- Here are some of the commonly used commands
```Python
# To add a new library to the project
poetry add <library>

# To remove a library from the project
poetry remove <library>

# To update library dependencies to the latest
poetry update

# To build the package (creates a wheel-based package distribution)
poetry build

# To publish the package 
poetry publish
```

## Conclusion

Poetry keeps project libraries' versions locked so there are no issues with libraries getting updated by mistake. It enforces virtual environments by default which is another good practice to keep project libraries isolated from the rest of the installed libraries in the environment.