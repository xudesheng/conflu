# Conflu

![Conflu icon](./assets/icon.png)

Conflu is a unified ThingWorx CLI and MCP server for agent-assisted ThingWorx development.

Public distribution:

- Releases: <https://github.com/xudesheng/conflu/releases>
- Latest release: <https://github.com/xudesheng/conflu/releases/latest>
- Install guide: [install.md](./install.md)
- MCP usage: [mcp.md](./mcp.md)
- Repository layout: [repo-layout.md](./repo-layout.md)
- Public release status: GitHub release notes status block or attached `distribution-state.json`

Release-status guidance:

- `public_ga` and `public_rc` mean core channels are healthy.
- `public_degraded` means at least one selected secondary channel is unhealthy or delayed.
- `revoked` means the release is no longer recommended because a core trust failure or rollback-triggering incident was recorded.

## Quick Install

```bash
npm i -g @xudesheng/conflu
conflu --version
```

For all install methods, see [install.md](./install.md).

## Quick Start

Create a Conflu repository:

```bash
conflu repo new test-repo
cd test-repo
```

Inspect available MCP tools:

```bash
conflu mcp list-tools
```

Register Conflu's MCP server with your coding assistant from a Conflu repository:

```bash
conflu mcp configure --print codex
conflu mcp configure --print cursor
conflu mcp configure --print claude
```

## Main Capabilities

- ThingWorx project layout scaffolding.
- ThingWorx entity validation, build, push, pull, and cache workflows.
- MCP tools for agent-assisted ThingWorx authoring and debugging.
- Optional Kepware MCP tools for simulator and configuration workflows.
- Built-in agent skill installation for supported coding assistants.
