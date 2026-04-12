# winforms-mcp plugin

Claude Code plugin wrapper for [**Rhombus.WinFormsMcp**](https://github.com/fnrhombus/winforms-mcp) — an MCP server that gives AI agents eyes and hands for Windows Forms apps.

This repo is just the plugin manifest. The server, docs, and issues all live in the [source repo](https://github.com/fnrhombus/winforms-mcp).

## Install

```
/install-plugin fnrhombus/winforms-mcp-plugin
```

## How it works

The plugin tells Claude Code to run `npx -y @fnrhombus/winforms-mcp`, which always fetches the latest version at runtime. Nothing here needs updating on release.

## License

[MIT](LICENSE)
