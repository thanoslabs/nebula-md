# nebula.md

[![CI](https://github.com/thanoslabs/nebula-md/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/thanoslabs/nebula-md/actions/workflows/deploy.yml)
[![Release](https://img.shields.io/github/v/release/thanoslabs/nebula-md?sort=semver&display_name=tag)](https://github.com/thanoslabs/nebula-md/releases/latest)
[![Docs site](https://img.shields.io/badge/docs-GitHub%20Pages-blue?logo=github)](https://thanoslabs.github.io/nebula-md/)

A static-site-generator for my obsidian vault.

## Goals

- [x] graph views
- [x] page linking
- [x] header parsing
- [x] light/dark mode
- [ ] plug-and-play
- [ ] ci/cd
- [ ] file and text search
- [ ] table contents

## Setup

```
# ./src
go run main.go
```

## Deployment

Once you've generated the files for your static page, the world is your oyster. For static hosting, I've largely relied on github pages since it's free.
