# winforms-mcp plugin

Claude Code plugin for [**Rhombus.WinFormsMcp**](https://github.com/fnrhombus/winforms-mcp) — an MCP server that gives AI agents eyes and hands for Windows Forms apps.

This repo is just the plugin manifest. The server, docs, and issues all live in the [source repo](https://github.com/fnrhombus/winforms-mcp).

## Install

**Step 1 — Add the marketplace** (one-time):

```
/plugin marketplace add fnrhombus/claude-plugins
```

**Step 2 — Install the plugin**:

```
/plugin install winforms-mcp@claude-plugins
```

Restart Claude Code and you're done. The plugin runs `npx -y @fnrhombus/winforms-mcp` under the hood — npm caches the package locally, so startup is fast after the first run.

## Forcing a fresh version

After a new release, npm may serve a cached copy. To force a fresh download:

```
npx -y @fnrhombus/winforms-mcp@latest
```

The plugin omits `@latest` in normal use to skip the registry check and start faster.

## License

[MIT](LICENSE)
