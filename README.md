# PortPirate Updates

Public signed Sparkle update feed and release artifacts for PortPirate.

[updates.johannesgrof.me](https://updates.johannesgrof.me/) serves the files in this repository through GitHub Pages.

## Purpose

This repo is intentionally boring infrastructure. It contains only public release artifacts that Sparkle and users are allowed to download. The PortPirate source code, signing setup, release workflow, and license logic live in the private app repository.

Update authenticity is enforced by Sparkle EdDSA signatures. Access control is handled inside the app through license activation and Pro feature gates, not by hiding the DMG or appcast.

## Layout

- `appcast.xml`
- `beta/appcast.xml`
- `releases/PortPirate-<version>.dmg`
- `releases/PortPirate-<version>.zip`
- `release-notes/<version>.md`
- `release-notes/<version>.html`

## Release Flow

Tagged releases are built in the private PortPirate repo. Its GitHub Action signs and notarizes the app, generates the Sparkle archive and appcast, then pushes the resulting static files here.

Manual edits should stay limited to this README, `index.html`, and emergency metadata corrections. Release artifacts should come from the private release workflow so appcast URLs, signatures, and checks stay reproducible.

## Public URLs

- Stable appcast: `https://updates.johannesgrof.me/appcast.xml`
- Beta appcast: `https://updates.johannesgrof.me/beta/appcast.xml`
- Downloads: `https://updates.johannesgrof.me/releases/`
- Release notes: `https://updates.johannesgrof.me/release-notes/`
