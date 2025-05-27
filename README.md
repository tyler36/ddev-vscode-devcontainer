[![tests](https://github.com/ddev/ddev-addon-template/actions/workflows/tests.yml/badge.svg)](https://github.com/ddev/ddev-addon-template/actions/workflows/tests.yml)

# ddev-vscode-devcontainer <!-- omit in toc -->

- [What is ddev-vscode-devcontainer?](#what-is-ddev-vscode-devcontainer)
- [Requirements](#requirements)
- [Getting started](#getting-started)
- [Usage](#usage)
  - [Open the web container](#open-the-web-container)
  - [Open the database container](#open-the-database-container)
- [Support](#support)
  - [Customization](#customization)

## What is ddev-vscode-devcontainer?

This addon adds a global helper function to open a running DDEV container in [VS Code](https://code.visualstudio.com/) (Visual Studio Code).

## Requirements

This addon has 3 main requirements:

- [DDEV](https://ddev.readthedocs.io/en/stable/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers), an extension for VS Code

Please see the relevant home pages above for installation and setup instructions.

## Getting started

1. Open a terminal to an existing project.
1. Install the `ddev-vscode-devcontainer` add-on:

   ```shell
   ddev add-on get tyler36/ddev-vscode-devcontainer
   ```

The command will become available after running `ddev start` or `ddev restart`.

## Usage

### Open the web container

```shell
ddev code
```

### Open the database container

```shell
ddev code -d
```

`-db` or `--database` may also be used.

## Support

The command assumes the VSCode executable (`code`) is available on your path.

WSL users may need to add the following to their `~/.bashrc` file.

   ```bash
   # Add default VSCODE install path to path
   export PATH="$PATH:/mnt/c/Program Files/Microsoft VS Code/bin"
   ```

### Customization

You can can customize the command by removing `#ddev-generated` from `~/.ddev/commands/host/code`.

Note, this will prevent DDEV from updating the command.

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
