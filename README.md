# Bloggr

A Spring Boot blog application with PostgreSQL database.

## Development Setup

### Prerequisites

- [Visual Studio Code](https://code.visualstudio.com/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) for VS Code

### Using the Dev Container

1. Clone this repository and open it in VS Code
2. When prompted "Reopen in Container", click it. Alternatively:
   - Press `F1` or `Ctrl+Shift+P`
   - Type "Reopen in Container" and select it

The dev container will:
- Set up Java (Microsoft OpenJDK)
- Set up PostgreSQL database
- Install necessary VS Code extensions
- Start the Spring Boot application automatically (via `gradle bootRun`)

### Ports

The following ports are automatically forwarded:
- `5432`: PostgreSQL database
- `8080`: Spring Boot application

### Java Development

The dev container comes with:
- Microsoft OpenJDK
- Gradle 8.13
- Pre-configured Java settings for optimal development
- Automatic null analysis
- Format on save enabled

#### Hot Reload with Spring DevTools

This project includes Spring DevTools which provides:
- Automatic restart when code changes are detected
- Live reload for template changes
- Enhanced development experience

When you make changes to your code:
1. Run `./gradlew build` or let your IDE build the project
2. Spring DevTools will automatically detect the changes
3. The application will restart with the new changes

Note: Template changes (in `src/main/resources/templates/`) will be reloaded without requiring a restart.

### Database Access

PostgreSQL is available at:
- Host: `localhost`
- Port: `5432`
- Default credentials are configured in the `application.yml` or `application-dev.yml` file

### Customization

You can modify the dev container configuration in:
- `.devcontainer/devcontainer.json`: Container settings, extensions, and VS Code preferences
- `.devcontainer/docker-compose.yml`: Docker services configuration

### Troubleshooting

If the application doesn't start automatically:
1. Open a terminal in VS Code
2. Run `./gradlew bootRun`

To rebuild the dev container:
1. Press `F1` or `Ctrl+Shift+P`
2. Type "Rebuild Container" and select it

