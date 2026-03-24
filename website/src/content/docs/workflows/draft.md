---
title: Draft Writing
description: Paper-style draft generation from research findings
section: Workflows
order: 7
---

## Usage

```
/draft <topic>
```

## What it does

Produces a paper-style draft with structured sections. Writes to `papers/`.

## Structure

The generated draft includes:

- Title
- Abstract
- Introduction / Background
- Method or Approach
- Evidence and Analysis
- Limitations
- Conclusion
- Sources

## Example

```
/draft survey of differentiable physics simulators
```

The writer agent works only from supplied evidence — it never fabricates content. If evidence is insufficient, it explicitly notes the gaps.
