---
title: Web Search
description: Web search routing and configuration
section: Tools
order: 2
---

## Routing modes

Feynman supports three web search backends:

| Mode | Description |
|------|-------------|
| `auto` | Prefer Perplexity when configured, fall back to Gemini |
| `perplexity` | Force Perplexity Sonar |
| `gemini` | Force Gemini (default) |

## Default behavior

The default path is zero-config Gemini Browser via a signed-in Chromium profile. No API keys required.

## Check current config

```bash
feynman search status
```

## Advanced configuration

Edit `~/.feynman/web-search.json` directly to set:

- Gemini API keys
- Perplexity API keys
- Custom routing preferences
