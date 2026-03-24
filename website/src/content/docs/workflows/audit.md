---
title: Code Audit
description: Compare paper claims against public codebases
section: Workflows
order: 4
---

## Usage

```
/audit <item>
```

## What it does

Compares claims made in a paper against its public codebase. Surfaces mismatches, missing experiments, and reproducibility risks.

## What it checks

- Do the reported hyperparameters match the code?
- Are all claimed experiments present in the repository?
- Does the training loop match the described methodology?
- Are there undocumented preprocessing steps?
- Do evaluation metrics match the paper's claims?

## Example

```
/audit 2401.12345
```

## Output

An audit report with:

- Claim-by-claim verification
- Identified mismatches
- Missing components
- Reproducibility risk assessment
