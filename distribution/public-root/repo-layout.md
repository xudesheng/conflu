# Conflu Repository Layout

Create a new repository:

```bash
conflu repo new test-repo
cd test-repo
```

Initial files:

```text
Conflu.toml
README.md
projects/
```

`Conflu.toml` is the repository manifest. `projects/` stores split-file ThingWorx project content.

## Validation

Run repository validation from the Conflu repository root:

```bash
conflu validate pkg
conflu validate dep
```

## Build

Build offline artifacts from split-file project content:

```bash
conflu build
```

## Live ThingWorx Workflows

Conflu supports live push/pull/cache workflows through environment profiles. Use development environments for write operations.

Inspect command help for the current profile and environment options:

```bash
conflu twx --help
conflu cache --help
conflu push --help
conflu pull --help
```

