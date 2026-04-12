# winforms-mcp-plugin

Claude Code plugin manifest for the [winforms-mcp](https://github.com/fnrhombus/winforms-mcp) MCP server. This repo contains only the plugin metadata — the actual server is distributed via npm (`@fnrhombus/winforms-mcp`) and NuGet (`Rhombus.WinFormsMcp`).

## How it works

This is an **MCP server plugin**, not a hooks plugin. The `.claude-plugin/plugin.json` declares an `mcpServers` entry that tells Claude Code to run `npx -y @fnrhombus/winforms-mcp` when the plugin is enabled. No hooks, no build step, no local code.

## Why nothing auto-updates

The `mcpServers` entry uses `npx -y @fnrhombus/winforms-mcp`, which always fetches the latest version from npm at runtime. There's nothing to version-bump here on release — the plugin repo is effectively static infrastructure.

## Discovery

The `claude-code-plugin` topic on this repo is what allows `fnrhombus/claude-plugins` (the central marketplace) to discover it. Don't remove the topic.
