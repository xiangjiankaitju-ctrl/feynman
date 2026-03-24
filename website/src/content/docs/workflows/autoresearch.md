---
title: Autoresearch
description: Autonomous experiment optimization loop
section: Workflows
order: 8
---

## Usage

```
/autoresearch <idea>
```

## What it does

Runs an autonomous experiment loop:

1. **Edit** — Modify code or configuration
2. **Commit** — Save the change
3. **Benchmark** — Run evaluation
4. **Evaluate** — Compare against baseline
5. **Keep or revert** — Persist improvements, roll back regressions
6. **Repeat** — Continue until the target is hit

## Tracking

Metrics are tracked in:

- `autoresearch.md` — Human-readable progress log
- `autoresearch.jsonl` — Machine-readable metrics over time

## Controls

```
/autoresearch <idea>     # start or resume
/autoresearch off        # stop, keep data
/autoresearch clear      # delete all state, start fresh
```

## Example

```
/autoresearch optimize the learning rate schedule for better convergence
```
