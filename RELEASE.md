# Release Guide

This document describes how to publish Poseigen packages to PyPI and create GitHub releases.

## Release Strategy

Release standalone packages first, then release the meta package.

Recommended order:

1. poseigen_seaside
2. poseigen_chisel
3. poseigen_compass
4. poseigen_binmeths
5. poseigen_trident
6. poseigen_mimic
7. poseigen_oyster
8. poseigen (meta package)

## Standalone Package Release

From each standalone package repository, create and push a version tag:

```bash
git tag 0.1.0
git push origin 0.1.0
```

Pre-release tags are also supported:

```bash
git tag 0.1.0rc1
git push origin 0.1.0rc1
```

Each package workflow builds, checks, publishes to PyPI, and creates a GitHub release.

## Meta Package Release

After all required standalone versions are on PyPI, release the meta package from this repository:

```bash
git tag poseigen-v0.1.0
git push origin poseigen-v0.1.0
```

Pre-release tag format:

```bash
git tag poseigen-v0.1.0rc1
git push origin poseigen-v0.1.0rc1
```

The meta workflow publishes poseigen and creates a GitHub release.

## Notes

- If a version already exists on PyPI, the workflow exits early.
- Keep package versions aligned with dependency compatibility across the suite.
