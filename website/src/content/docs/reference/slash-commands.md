---
title: Slash Commands
description: Repo-owned REPL slash commands
section: Reference
order: 2
---

This page documents the slash commands that Feynman owns in this repository: prompt templates from `prompts/` and extension commands from `extensions/research-tools/`.

Additional slash commands can appear at runtime from Pi core and bundled packages such as subagents, preview, session search, and scheduling. Use `/help` inside the REPL for the live command list instead of relying on a static copy of package-provided commands.

## Research Workflows

| Command | Description |
| --- | --- |
| `/deepresearch <topic>` | Run a thorough, source-heavy investigation on a topic and produce a durable research brief with inline citations. |
| `/lit <topic>` | Run a literature review on a topic using paper search and primary-source synthesis. |
| `/review <artifact>` | Simulate an AI research peer review with likely objections, severity, and a concrete revision plan. |
| `/audit <item>` | Compare a paper's claims against its public codebase and identify mismatches, omissions, and reproducibility risks. |
| `/replicate <paper>` | Plan or execute a replication workflow for a paper, claim, or benchmark. |
| `/compare <topic>` | Compare multiple sources on a topic and produce a source-grounded matrix of agreements, disagreements, and confidence. |
| `/draft <topic>` | Turn research findings into a polished paper-style draft with equations, sections, and explicit claims. |
| `/autoresearch <idea>` | Autonomous experiment loop — try ideas, measure results, keep what works, discard what doesn't, repeat. |
| `/watch <topic>` | Set up a recurring or deferred research watch on a topic, company, paper area, or product surface. |

## Project & Session

| Command | Description |
| --- | --- |
| `/log` | Write a durable session log with completed work, findings, open questions, and next steps. |
| `/jobs` | Inspect active background research work, including running processes and scheduled follow-ups. |
| `/help` | Show grouped Feynman commands and prefill the editor with a selected command. |
| `/init` | Bootstrap AGENTS.md and session-log folders for a research project. |

## Setup

| Command | Description |
| --- | --- |
| `/alpha-login` | Sign in to alphaXiv from inside Feynman. |
| `/alpha-status` | Show alphaXiv authentication status. |
| `/alpha-logout` | Clear alphaXiv auth from inside Feynman. |
