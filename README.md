# Core Development Container for Japanese developers

[![Docker Image Version (latest semver)](https://img.shields.io/docker/v/json777/core-dev-container-jp?sort=semver)](https://hub.docker.com/r/json777/core-dev-container-jp)
[![Docker Image Size (latest semver)](https://img.shields.io/docker/image-size/json777/core-dev-container-jp?sort=semver)](https://hub.docker.com/r/json777/core-dev-container-jp)

## Overview
This is a base development container called **Core**, specifically designed for the Japanese development environment. It is built using Ubuntu and includes essential development tools like `zsh`, `oh-my-zsh`, `git`, and `Homebrew`. The container is configured with Japanese locale settings (`ja_JP.UTF-8`) and the timezone set to Asia/Tokyo (UTC+9). This container serves as a base for adding various programming languages and development tools tailored for developers in Japan.

## Features
- Base: Ubuntu
- Shell: `zsh` with `oh-my-zsh`
- Includes essential tools: `git`, `gh`, `vim`, `build-essential`, etc.
- Homebrew installed for easy package management
- Locale set to Japanese (`ja_JP.UTF-8`)
- Timezone set to Asia/Tokyo (UTC+9)

## How to Use
### Using the Container as a Base

You can use this container as a starting point for your development environment. By extending this base container, you can add specific tools and dependencies required for your projects. Below is an example of how to extend this container to include Python.

```Dockerfile
FROM json777/core-dev-container-jp:latest

# Example of adding Python
RUN apt-get update && \
    apt-get install -y python3 python3-pip
```

# License

This project is licensed under the MIT License.
