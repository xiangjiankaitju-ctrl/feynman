---
name: agentcomputer
description: Delegate research tasks to remote Agent Computer machines for cloud execution. Manages machine discovery, remote agent sessions, task delegation, progress monitoring, result retrieval, and ACP bridging via the aicomputer CLI.
allowed-tools: Bash(npm:*), Bash(npx aicomputer@latest:*), Bash(aicomputer:*), Bash(computer:*)
---

# Agent Computer

Use Agent Computer to run Feynman research workflows on remote cloud machines when local compute is insufficient or when tasks should run unattended.

## When to use

- A research task needs GPU, large memory, or long-running compute
- `/autoresearch` or `/deepresearch` should run unattended in the cloud
- The user explicitly asks to delegate work to a remote machine
- An experiment loop would take hours and should not block the local session

## Prerequisites

The `aicomputer` CLI must be installed and authenticated:

```bash
if command -v computer >/dev/null 2>&1; then
  COMPUTER=computer
elif command -v aicomputer >/dev/null 2>&1; then
  COMPUTER=aicomputer
else
  npm install -g aicomputer
  COMPUTER=computer
fi
$COMPUTER whoami || $COMPUTER login
```

## Fleet control

### Discover machines and agents

```bash
$COMPUTER ls --json
$COMPUTER agent agents <machine> --json
```

### Sessions

Create, reuse, and manage named sessions on a machine:

```bash
$COMPUTER agent sessions new <machine> --agent claude --name research --json
$COMPUTER agent sessions list <machine> --json
$COMPUTER agent status <machine> --session <session_id> --json
```

### Prompting and monitoring

```bash
$COMPUTER agent prompt <machine> "<task>" --agent claude --name research
$COMPUTER agent watch <machine> --session <session_id>
```

### Stopping and cleanup

```bash
$COMPUTER agent cancel <machine> --session <session_id> --json
$COMPUTER agent interrupt <machine> --session <session_id> --json
$COMPUTER agent close <machine> --session <session_id>
```

## Research delegation workflow

1. Pick a machine: `$COMPUTER ls --json`
2. Create a session: `$COMPUTER agent sessions new <machine> --agent claude --name research --json`
3. Send a self-contained research prompt:

```bash
$COMPUTER agent prompt <machine> \
  "Run a deep research workflow on <topic>. Write all outputs to /workspace/outputs/. When done, write a summary to /workspace/outputs/summary.md." \
  --agent claude --name research
```

4. Monitor: `$COMPUTER agent watch <machine> --session <session_id>`
5. Retrieve: `$COMPUTER agent prompt <machine> "cat /workspace/outputs/summary.md" --session <session_id>`
6. Clean up: `$COMPUTER agent close <machine> --session <session_id>`

## ACP bridge

Expose a remote machine agent as a local ACP-compatible stdio process:

```bash
$COMPUTER acp serve <machine> --agent claude --name research
```

This lets local ACP clients (including Feynman's subagents) talk to a remote agent as if it were local. Keep the bridge process running; reconnect by restarting the command with the same session name.

## Session naming

Use short stable names that match the task:

- `research` — general research delegation
- `experiment` — autoresearch loops
- `review` — verification passes
- `literature` — literature sweeps

Reuse the same name when continuing the same line of work.

## References

- [CLI cheatsheet](references/cli-cheatsheet.md) — full command reference
- [ACP flow](references/acp-flow.md) — protocol details for the ACP bridge
