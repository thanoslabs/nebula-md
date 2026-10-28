# nebula.md

[![CI](https://github.com/thanoslabs/nebula-md/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/thanoslabs/nebula-md/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/thanoslabs/nebula-md?sort=semver&display_name=tag)](https://github.com/thanoslabs/nebula-md/releases/latest)
[![Docs site](https://img.shields.io/badge/docs-GitHub%20Pages-blue?logo=github)](https://thanoslabs.github.io/nebula-md/)

A static-site-generator for my obsidian vault.

## Goals

- [x] graph views
- [x] page linking
- [x] header parsing
- [x] light/dark mode
- [ ] plug-and-play
- [x] ci/cd
- [ ] file and text search
- [ ] table contents

## Setup

```
# ./src
go run main.go
```

## Deployment

Once you've generated the files for your static page, the world is your oyster. For static hosting, I've largely relied on github pages since it's free.


## CI and releases

Pull requests and pushes to `main` run Go module verification, formatting, vet, race-enabled tests and a binary build using the Go version specified in `src/go.mod`.

Releases follow the `thanoslabs/template-repo` convention: merging to `main` creates a bare SemVer `X.Y.Z` tag and GitHub release. The merged PR's `major` or `minor` label sets the bump (major wins); otherwise it increments the patch version. The **Release** workflow also supports manual dispatch with an explicit version.

The reusable `.github/workflows/deploy.yml` can be pinned at a release, for example `thanoslabs/nebula-md/.github/workflows/deploy.yml@1.2.3`. A release version freezes both the generator source and reusable workflow for callers; update the version deliberately to adopt changes.
