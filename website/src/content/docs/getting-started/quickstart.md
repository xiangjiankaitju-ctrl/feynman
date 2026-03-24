---
title: Quick Start
description: Get up and running with Feynman in 60 seconds
section: Getting Started
order: 2
---

## First run

```bash
feynman setup
feynman
```

`feynman setup` walks you through model authentication, alphaXiv login, web search configuration, and preview dependencies.

## Ask naturally

Feynman routes your questions into the right workflow automatically. You don't need slash commands to get started.

```
> What are the main approaches to RLHF alignment?
```

Feynman will search papers, gather web sources, and produce a structured answer with citations.

## Use workflows directly

For explicit control, use slash commands inside the REPL:

```
> /deepresearch transformer scaling laws
> /lit multimodal reasoning benchmarks
> /review paper.pdf
```

## Output locations

Feynman writes durable artifacts to canonical directories:

- `outputs/` — Reviews, reading lists, summaries
- `papers/` — Polished paper-style drafts
- `experiments/` — Runnable code and result logs
- `notes/` — Scratch notes and session logs
