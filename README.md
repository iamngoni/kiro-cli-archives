# kiro-cli-archives

This repository republishes the official Kiro macOS archive as a versioned `.zip`
containing `Kiro CLI.app` so the app bundle can be consumed from a standard
extractable archive.

The workflow reads the official manifest at:

- `https://prod.download.cli.kiro.dev/stable/latest/manifest.json`

Then it:

1. Resolves the official macOS `.dmg` entry.
2. Downloads and mounts the disk image on a macOS runner.
3. Copies the `.app` bundle into a `.zip`.
4. Publishes a GitHub release tagged with the upstream version.

Manual runs can override the manifest URL via `workflow_dispatch`.
