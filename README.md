# phoenix

[![Build](https://github.com/gsmlg-ci/phoenix/actions/workflows/build.yml/badge.svg)](https://github.com/gsmlg-ci/phoenix/actions/workflows/build.yml)

Docker image for [Phoenix Framework](https://www.phoenixframework.org/) development, built on top of Elixir with Node.js, Bun, and Tailwind CSS pre-installed.

**Current versions:**
- Elixir: 1.19.5
- Phoenix: 1.8.3
- Node.js: 22.x
- Bun: latest
- Tailwind CSS: latest

Docker image published to:
- `docker.io/gsmlg/phoenix`
- `ghcr.io/gsmlg-dev/phoenix`

## Tags

- `latest` / `1.8.3` — Debian-based
- `alpine` / `1.8.3-alpine` — Alpine-based

## Usage

```bash
# From Docker Hub
docker pull gsmlg/phoenix:latest

# From GitHub Container Registry
docker pull ghcr.io/gsmlg-dev/phoenix:latest

# Create a new Phoenix project
docker run --rm -v $(pwd):/app -w /app gsmlg/phoenix:latest "mix phx.new my_app"
```

## Build

```bash
# Debian-based
docker build --build-arg ELIXIR_VERSION=1.19.5 --build-arg PHOENIX_VERSION=1.8.3 -t gsmlg/phoenix .

# Alpine-based
docker build --build-arg ELIXIR_VERSION=1.19.5 --build-arg PHOENIX_VERSION=1.8.3 -f Dockerfile.alpine -t gsmlg/phoenix:alpine .
```
