---
title: Installation
description: Install Feynman on macOS, Linux, or Windows using the one-line installer or npm.
section: Getting Started
order: 1
---

Feynman ships as a standalone binary for macOS and Linux, and as an npm package for all platforms including Windows. The recommended approach is the one-line installer, which downloads a prebuilt native binary with zero dependencies.

## One-line installer (recommended)

On **macOS or Linux**, open a terminal and run:

```bash
curl -fsSL https://feynman.is/install | bash
```

The installer detects your OS and architecture automatically. On macOS it supports both Intel and Apple Silicon. On Linux it supports x64 and arm64. The binary is installed to `~/.feynman/bin` and added to your `PATH`.

On **Windows**, open PowerShell as Administrator and run:

```powershell
irm https://feynman.is/install.ps1 | iex
```

This installs the native Windows binary and adds Feynman to your user `PATH`. You can re-run either installer at any time to update to the latest version.

## npm / npx

If you already have Node.js 18+ installed, you can install Feynman globally via npm:

```bash
npm install -g @companion-ai/feynman
```

Or run it directly without installing:

```bash
npx @companion-ai/feynman
```

The npm distribution bundles the same core runtime as the native installer but depends on Node.js being present on your system. The native installer is preferred because it ships a self-contained binary with faster startup.

## Post-install setup

After installation, run the guided setup wizard to configure your model provider and API keys:

```bash
feynman setup
```

This walks you through selecting a default model, authenticating with your provider, and optionally installing extra packages for features like web search and document preview. See the [Setup guide](/docs/getting-started/setup) for a detailed walkthrough.

## Verifying the installation

Confirm Feynman is installed and accessible:

```bash
feynman --version
```

If you see a version number, you are ready to go. Run `feynman doctor` at any time to diagnose configuration issues, missing dependencies, or authentication problems.

## Local development

For contributing or running Feynman from source:

```bash
git clone https://github.com/getcompanion-ai/feynman.git
cd feynman
npm install
npm run start
```
