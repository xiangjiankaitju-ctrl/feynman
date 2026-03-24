---
title: Configuration
description: Configure models, search, and runtime options
section: Getting Started
order: 4
---

## Model

Set the default model:

```bash
feynman model set <provider:model>
```

Override at runtime:

```bash
feynman --model anthropic:claude-opus-4-6
```

List available models:

```bash
feynman model list
```

## Thinking level

Control the reasoning depth:

```bash
feynman --thinking high
```

Levels: `off`, `minimal`, `low`, `medium`, `high`, `xhigh`.

## Web search

Check the current search configuration:

```bash
feynman search status
```

For advanced configuration, edit `~/.feynman/web-search.json` directly to set Gemini API keys, Perplexity keys, or a different route.

## Working directory

```bash
feynman --cwd /path/to/project
```

## Session storage

```bash
feynman --session-dir /path/to/sessions
```

## One-shot mode

Run a single prompt and exit:

```bash
feynman --prompt "summarize the key findings of 2401.12345"
```
