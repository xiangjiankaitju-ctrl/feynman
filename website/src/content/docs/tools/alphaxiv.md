---
title: AlphaXiv
description: Search and retrieve academic papers through the AlphaXiv integration.
section: Tools
order: 1
---

AlphaXiv is the primary academic paper search and retrieval tool in Feynman. It provides access to a vast corpus of research papers, discussion threads, citation metadata, and full-text PDFs. The researcher agent uses AlphaXiv as its primary source for academic content.

## Authentication

AlphaXiv requires authentication. Set it up during initial setup or at any time:

```bash
feynman alpha login
```

Check your authentication status:

```bash
feynman alpha status
```

You can also manage AlphaXiv auth from inside the REPL with `/alpha-login`, `/alpha-status`, and `/alpha-logout`.

## What it provides

AlphaXiv gives Feynman access to several capabilities that power the research workflows:

- **Paper search** -- Find papers by topic, author, keyword, or arXiv ID
- **Full-text retrieval** -- Download and parse complete PDFs for in-depth reading
- **Citation metadata** -- Access citation counts, references, and citation chains
- **Discussion threads** -- Read community discussions and annotations on papers
- **Related papers** -- Discover connected work through citation graphs and recommendations

## How it is used

You do not invoke AlphaXiv directly in most cases. The researcher agent uses it automatically during workflows like deep research, literature review, and peer review. When you provide an arXiv ID (like `arxiv:2401.12345`), Feynman fetches the paper through AlphaXiv.

AlphaXiv search is especially powerful when combined with citation chaining. The researcher agent can follow references from a relevant paper to discover foundational work, then follow forward citations to find papers that built on it. This produces a much more complete picture than keyword search alone.

## Configuration

AlphaXiv configuration is managed through the CLI commands listed above. Authentication tokens are stored in `~/.feynman/auth/` and persist across sessions. No additional configuration is needed beyond logging in.

## Without AlphaXiv

If you choose not to authenticate with AlphaXiv, Feynman still functions but with reduced academic search capabilities. It falls back to web search for finding papers, which works for well-known work but misses the citation metadata, discussion threads, and full-text access that AlphaXiv provides. For serious research workflows, AlphaXiv authentication is strongly recommended.
