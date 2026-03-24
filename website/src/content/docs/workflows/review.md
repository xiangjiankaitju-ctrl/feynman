---
title: Peer Review
description: Simulated peer review with severity-graded feedback
section: Workflows
order: 3
---

## Usage

```
/review <artifact>
```

## What it does

Simulates a tough-but-fair peer review for AI research artifacts. Evaluates novelty, empirical rigor, baselines, ablations, and reproducibility.

The reviewer agent identifies:

- Weak baselines
- Missing ablations
- Evaluation mismatches
- Benchmark leakage
- Under-specified implementation details

## Severity levels

Feedback is graded by severity:

- **FATAL** — Fundamental issues that invalidate the claims
- **MAJOR** — Significant problems that need addressing
- **MINOR** — Small improvements or clarifications

## Example

```
/review outputs/scaling-laws-brief.md
```

## Output

Structured review with:

- Summary of the work
- Strengths
- Weaknesses (severity-graded)
- Questions for the authors
- Verdict (accept / revise / reject)
- Revision plan
