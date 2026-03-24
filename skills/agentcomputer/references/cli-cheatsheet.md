# CLI Cheatsheet

## Authentication

```bash
computer whoami
computer login
computer claude-login     # install Claude credentials on a machine
computer codex-login      # install Codex credentials on a machine
```

## Machine discovery

```bash
computer ls --json
computer fleet status --json
```

## Agent discovery

```bash
computer agent agents <machine> --json
```

## Sessions

```bash
computer agent sessions list <machine> --json
computer agent sessions new <machine> --agent claude --name research --json
computer agent status <machine> --session <session_id> --json
```

## Prompting

```bash
computer agent prompt <machine> "run the experiment" --agent claude --name research
computer agent prompt <machine> "continue" --session <session_id>
```

## Streaming and control

```bash
computer agent watch <machine> --session <session_id>
computer agent cancel <machine> --session <session_id> --json
computer agent interrupt <machine> --session <session_id> --json
computer agent close <machine> --session <session_id>
```

## ACP bridge

```bash
computer acp serve <machine> --agent claude --name research
```

## Machine lifecycle

```bash
computer create my-box
computer open my-box
computer open my-box --terminal
computer ssh my-box
```

## Good defaults

- Prefer machine handles over machine ids when both are available.
- Prefer `--name` for human-meaningful persistent sessions.
- Prefer `--json` when another program or agent needs to read the result.
