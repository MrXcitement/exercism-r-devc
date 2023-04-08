# Exercism R

 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview
A Dev Container project for the [Exercism R track](https://exercism.org/tracks/r). It defines a Dev Container with the Exercism cli and the [R Project](https://www.r-project.org/) installed.

The project is designed to allows you to work through the Exercism R track exercises using the Visual Studio Code editor and the Dev Container running either in a local Docker instance, a remote Docker instance or in a GitHub Codespaces environment.

The project expects that your Exercism tracks will be downloaded to the `exercism-r/r` subfolder. This folder is ignored and not versioned with this project. If you wish to also keep your exercise solutions in `git` it is recommended that you either version the `exercisim-r/r` subfolder or each downloaded tracks subfolder that you work on.

## Requirements
It is expected that:
- You are familiar with VS Code
- You have installed *VS Code's Remote extensions*.
- You have an Exercism account.

You need to have installed on your computer:
- Visual Studio Code
- Git

### Local Dev Container
To host the Dev Container locally:
- Container Engine
  - Windows: Docker Desktop 2.0+ on Windows 10/11 Pro/Enterprise.
  - macOS: Docker Desktop 2.0+
  - Linux: Docker CE/EE 18.06+ and Docker Compose 1.21+.

### Remote Dev Container
To host the Dev Container remotely:
- Container Engine
  - Linux: Docker CE/EE 18.06+ and Docker Compose 1.21+.
- 2 GB RAM and a 2-core CPU is recommended.

### GitHub Codespace Dev Container
To host the Dev Container in a GitHub Codespace:
- You can use the Codespace remotely via the VSCode online editor and have no requirements.
- You can connect a local VSCode instance to the remote Codespace using the [GitHub Codespaces extension](https://marketplace.visualstudio.com/items?itemName=GitHub.codespaces).

## Use
- Clone this repository.
- Open the repository in Visual Studio Code.
- Reopen in Container. (`Dev Containers: Reopen in Container`)
- Open a terminal inside the container. (`View: Toggle Terminal` <kbd>Ctrl</kbd>+<kbd>`</kbd>)
- Configure the exercism cli with your token and set the workspace folder to the root folder of this project.
  ```sh
  $ exercism configure -t <your token> -w "$PWD"
  ```
- Use the exercism cli to download the exercise to work on from the R track.
  ```sh
  $ exercism download -t r -e hello-world
  ```
- Edit the provided exercise file until the provided tests pass.
- Submit your solved exercise.
  ```sh
  $ exercism submit src/HelloWorld.hs
  ```

## Related Projects
- [Exercism R Track](https://exercism.org/tracks/r)
- [Debian Packages of R Software](https://cran.r-project.org/bin/linux/debian)
- [R Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=REditorSupport.r)
- [R Debugger for VS Code](https://marketplace.visualstudio.com/items?itemName=RDebugger.r-debugger)
- [Dev Containers](https://containers.dev/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Docker Engine](https://docs.docker.com/engine/)
- [GitHub Codespaces](https://docs.github.com/en/codespaces)
- [Visual Studio Code Developing inside a Container](https://code.visualstudio.com/docs/devcontainers/containers)
