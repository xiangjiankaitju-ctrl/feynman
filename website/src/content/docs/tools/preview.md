---
title: Preview
description: Preview generated artifacts in browser or PDF
section: Tools
order: 4
---

## Overview

The `preview_file` tool opens generated artifacts in your browser or PDF viewer.

## Usage

Inside the REPL:

```
/preview
```

Or Feynman will suggest previewing when you generate artifacts that benefit from rendered output (Markdown with LaTeX, HTML reports, etc.).

## Requirements

Preview requires `pandoc` for PDF/HTML rendering. Install it with:

```bash
feynman --setup-preview
```

## Supported formats

- Markdown (with LaTeX math rendering)
- HTML
- PDF
