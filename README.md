# Luxium + Embeddium — Minecraft 26.2 / Forge 65.1.0

## ⬇️ Download 26.2 (Forge 65.1.0) — DEV ONLY

**[Download placeholder JAR bundle (.zip)](https://github.com/peecer/Luxiom-Embedium-26.2-Forge-65.1.0/releases/download/unimplemented-bootstrap-0.0.0-dev/UNIMPLEMENTED-MC-26.2-Forge-65.1.0-BUNDLE.zip)** | **[Individual JAR downloads](https://github.com/peecer/Luxiom-Embedium-26.2-Forge-65.1.0/blob/main/DOWNLOADS.md)** | **[GitHub prerelease](https://github.com/peecer/Luxiom-Embedium-26.2-Forge-65.1.0/releases/tag/unimplemented-bootstrap-0.0.0-dev)**

> ⚠️ **Not playable mods:** The binaries currently contain loader entrypoints only. Luxium's lighting/shaders and Embeddium's renderer are **not implemented**. Do not treat these as finished versions.

> **WORK IN PROGRESS / NO PLAYABLE RELEASE** — This GitHub repository now includes a Gradle project and compilation bootstraps, but it does **not** contain the original renderer, shaders, mixins or any functional features.

This repository has two port targets, **Luxium** (originally Forge 1.20.1 by Vinlanx) and **Embeddium** (original Fabric 1.20.1 binary supplied by the requester). Both must be ported to Minecraft 26.2 / Forge 65.1.0; Java 25 is required.

## Repository contents

- `src/main/java`: two Forge mod entrypoint placeholders.
- `src/main/resources/META-INF/mods.toml`: Forge mod descriptors.
- `build.gradle` and `gradle.properties`: ForgeGradle development setup.
- `.github/workflows/gradle.yml`: compile verification on pushes and PRs.
- `docs/BINARY_AUDIT.md`: hashes, old dependency mismatch and provenance.
- `PORT_STATUS.md`: feature and validation checklist.

## Build setup

1. Install Java 25 and Gradle 9.6.0, then run `gradle build` (or generate the Gradle wrapper first).
2. Check GitHub Actions for compilation results.
3. **Do not install generated JARs as working mods.** These bootstraps only show how the mod loader can load basic entrypoints.

## Port milestones

1. Import authorized, **editable source** for Luxium and the corresponding Embeddium branch; preserve applicable copyright/license notices.
2. Port shader resources, options GUI, renderer hooks and mixin targets to 26.2.
3. Rework Luxium-Embeddium integration and dependency/version declarations, including the old binaries' mismatch detailed in the audit.
4. Compile, launch in Minecraft, test graphics and world loading, then prepare actual releases.

**A Gradle bootstrap is not a fork of the full implementation.** All inherited original features are currently absent.
