# DockerSQL

A simple CLI wrapper for managing a MySQL + phpMyAdmin Docker setup.

## Features

- Start/stop MySQL easily
- Optional phpMyAdmin UI
- Quick access to MySQL CLI
- Clean environment-based config

---

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/dockersql.git
cd dockersql
```

### 2. Add `dockersql` to your global PATH (zsh)

Make sure the script is executable, then add this project directory to your PATH in `~/.zshrc`:

```bash
chmod +x dockersql
echo "export PATH=\"$PATH:$(pwd)\"" >> ~/.zshrc
source ~/.zshrc
```

After this, you can run `dockersql` from anywhere.

## Usage

### Commands and switches

| Command                    | Description                |
| -------------------------- | -------------------------- |
| `dockersql -start`         | Start MySQL only           |
| `dockersql -start --web`   | Start MySQL + phpMyAdmin   |
| `dockersql -restart`       | Restart MySQL only         |
| `dockersql -restart --web` | Restart MySQL + phpMyAdmin |
| `dockersql -stop`          | Stop all containers        |
| `dockersql -status`        | Show container status      |
| `dockersql -logs`          | Show logs                  |
| `dockersql`                | Open MySQL CLI             |

### Quick examples

```bash
dockersql -start
dockersql -start --web
dockersql -restart
dockersql -restart --web
dockersql -stop
dockersql -status
dockersql -logs
dockersql
```
