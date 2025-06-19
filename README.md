# Java Dev Container Submodule

This submodule provides a ready-to-use [Development Container](https://containers.dev/) setup for Java projects. It is designed to be included as a Git submodule in your repository, enabling a consistent and reproducible Java development environment across different machines and teams.

## Features

- Pre-installed OpenJDK (version configurable)
- Maven and/or Gradle support
- Common Java development tools
- VS Code Dev Container configuration

## Usage

1. **Add as a submodule**  
    ```sh
    git submodule add <repository-url> .submodules/java-dev-container
    git submodule update --init --recursive
    ```

2. **Reference the devcontainer**  
    In your project's `.devcontainer/devcontainer.json`, reference the configuration from this submodule:
    ```json
    {
      "extends": "../.submodules/java-devcontainer/devcontainer.json"
    }
    ```

3. **Open in Dev Container**  
    Open your project in [VS Code](https://code.visualstudio.com/) and reopen in the container when prompted.

## GitHub SSH Key Integration

During the initial setup, the dev container automatically generates an SSH key pair for secure integration with GitHub. After the container starts, the public SSH key is printed in the terminal.

**To enable GitHub integration:**

1. Copy the public SSH key displayed in the terminal after the container starts.
2. Go to your [GitHub SSH keys settings](https://github.com/settings/keys).
3. Click **"New SSH key"**, give it a descriptive title, and paste the copied key.
4. Save the new key.

This allows the dev container to authenticate with GitHub for cloning, pushing, and pulling repositories.

## Customization

You can override or extend the base configuration by adding your own settings in your project's `.devcontainer` folder.

## Updating

To update the submodule to the latest version:
```sh
git submodule update --remote .submodules/java-devcontainer
```

## License

See [LICENSE](./LICENSE) for details.
