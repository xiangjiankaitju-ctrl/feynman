---
title: CLI Commands
description: Complete reference for Feynman CLI commands
section: Reference
order: 1
---

This page covers the dedicated Feynman CLI commands and compatibility flags.

Workflow prompt templates such as `/deepresearch` also run directly from the shell as `feynman <workflow> ...`. Those workflow entries live in the slash-command reference instead of being duplicated here.

## Core

| Command | Description |
| --- | --- |
| `feynman` | Launch the interactive REPL. |
| `feynman chat [prompt]` | Start chat explicitly, optionally with an initial prompt. |
| `feynman help` | Show CLI help. |
| `feynman setup` | Run the guided setup wizard. |
| `feynman doctor` | Diagnose config, auth, Pi runtime, and preview dependencies. |
| `feynman status` | Show the current setup summary. |

## Model Management

| Command | Description |
| --- | --- |
| `feynman model list` | List available models in Pi auth storage. |
| `feynman model login [id]` | Login to a Pi OAuth model provider. |
| `feynman model logout [id]` | Logout from a Pi OAuth model provider. |
| `feynman model set <provider/model>` | Set the default model. |

## AlphaXiv

| Command | Description |
| --- | --- |
| `feynman alpha login` | Sign in to alphaXiv. |
| `feynman alpha logout` | Clear alphaXiv auth. |
| `feynman alpha status` | Check alphaXiv auth status. |

## Utilities

| Command | Description |
| --- | --- |
| `feynman search status` | Show Pi web-access status and config path. |
| `feynman update [package]` | Update installed packages, or a specific package. |

## Flags

| Flag | Description |
| --- | --- |
| `--prompt "<text>"` | Run one prompt and exit. |
| `--alpha-login` | Sign in to alphaXiv and exit. |
| `--alpha-logout` | Clear alphaXiv auth and exit. |
| `--alpha-status` | Show alphaXiv auth status and exit. |
| `--model <provider:model>` | Force a specific model. |
| `--thinking <level>` | Set thinking level: off | minimal | low | medium | high | xhigh. |
| `--cwd <path>` | Set the working directory for tools. |
| `--session-dir <path>` | Set the session storage directory. |
| `--new-session` | Start a new persisted session. |
| `--doctor` | Alias for `feynman doctor`. |
| `--setup-preview` | Alias for `feynman setup preview`. |
