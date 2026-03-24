---
title: Deep Research
description: Thorough source-heavy investigation with parallel agents
section: Workflows
order: 1
---

## Usage

```
/deepresearch <topic>
```

## What it does

Deep research runs a thorough, source-heavy investigation. It plans the research scope, delegates to parallel researcher agents, synthesizes findings, and adds inline citations.

The workflow follows these steps:

1. **Plan** — Clarify the research question and identify search strategy
2. **Delegate** — Spawn parallel researcher agents to gather evidence from different source types (papers, web, repos)
3. **Synthesize** — Merge findings, resolve contradictions, identify gaps
4. **Cite** — Add inline citations and verify all source URLs
5. **Deliver** — Write a durable research brief to `outputs/`

## Example

```
/deepresearch transformer scaling laws and their implications for compute-optimal training
```

## Output

Produces a structured research brief with:

- Executive summary
- Key findings organized by theme
- Evidence tables with source links
- Open questions and suggested next steps
- Numbered sources section with direct URLs
