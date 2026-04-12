# winforms-mcp plugin

Claude Code plugin wrapper for [**Rhombus.WinFormsMcp**](https://github.com/fnrhombus/winforms-mcp) — an MCP server that gives AI agents eyes and hands for Windows Forms apps.

This repo is just the plugin manifest. The server, docs, and issues all live in the [source repo](https://github.com/fnrhombus/winforms-mcp).

## Install

```
/install-plugin fnrhombus/winforms-mcp-plugin
```

## How it works

The plugin tells Claude Code to run `npx -y @fnrhombus/winforms-mcp`. npm caches the package locally, so after a new release you may need to clear the cache to pick it up:

```
npx clear-npx-cache
```

## License

[MIT](LICENSE)
