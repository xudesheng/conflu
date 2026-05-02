# Conflu MCP

Conflu can run as a Model Context Protocol server over stdio.

## List Tools

```bash
conflu mcp list-tools
```

## Serve MCP

```bash
conflu mcp serve
```

Enable Kepware tools explicitly:

```bash
conflu mcp --kepware serve
```

## Configure Coding Assistants

From a Conflu repository, print the MCP config change before writing it:

```bash
conflu mcp configure --print codex
conflu mcp configure --print cursor
conflu mcp configure --print claude
```

Then apply the desired target:

```bash
conflu mcp configure codex
```

Pass `--kepware` on the parent `mcp` command when you want Kepware tools included:

```bash
conflu mcp --kepware configure --print codex
```

