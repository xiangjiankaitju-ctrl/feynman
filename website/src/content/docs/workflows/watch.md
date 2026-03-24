---
title: Watch
description: Recurring research monitoring
section: Workflows
order: 9
---

## Usage

```
/watch <topic>
```

## What it does

Schedules a recurring research watch. Sets a baseline of current knowledge and defines what constitutes a meaningful change worth reporting.

## Example

```
/watch new papers on test-time compute scaling
```

## How it works

1. Feynman establishes a baseline by surveying current sources
2. Defines change signals (new papers, updated results, new repos)
3. Schedules periodic checks via `pi-schedule-prompt`
4. Reports only when meaningful changes are detected
