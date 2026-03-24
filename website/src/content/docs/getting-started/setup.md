---
title: Setup
description: Detailed setup guide for Feynman
section: Getting Started
order: 3
---

## Guided setup

```bash
feynman setup
```

This walks through four steps:

### Model provider authentication

Feynman uses Pi's OAuth system for model access. The setup wizard prompts you to log in to your preferred provider.

```bash
feynman model login
```

### AlphaXiv login

AlphaXiv powers Feynman's paper search and analysis tools. Sign in with:

```bash
feynman alpha login
```

Check status anytime:

```bash
feynman alpha status
```

### Web search routing

Feynman supports three web search backends:

- **auto** — Prefer Perplexity when configured, fall back to Gemini
- **perplexity** — Force Perplexity Sonar
- **gemini** — Force Gemini (default, zero-config via signed-in Chromium)

The default path requires no API keys — it uses Gemini Browser via your signed-in Chromium profile.

### Preview dependencies

For PDF and HTML export of generated artifacts, Feynman needs `pandoc`:

```bash
feynman --setup-preview
```

Global macOS installs also try to install pandoc automatically when Homebrew is available. Use the command above to retry manually.

### Optional packages

Feynman keeps the default package set lean so first-run installs stay fast. Install the heavier optional packages only when you need them:

```bash
feynman packages list
feynman packages install memory
feynman packages install session-search
feynman packages install generative-ui
feynman packages install all-extras
```

## Diagnostics

Run the doctor to check everything:

```bash
feynman doctor
```

This verifies model auth, alphaXiv credentials, preview dependencies, and the Pi runtime.
