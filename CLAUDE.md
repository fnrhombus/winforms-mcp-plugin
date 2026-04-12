# winforms-mcp-plugin

Claude Code plugin manifest for the [winforms-mcp](https://github.com/fnrhombus/winforms-mcp) MCP server. This repo contains only the plugin metadata — the actual server is distributed via npm (`@fnrhombus/winforms-mcp`) and NuGet (`Rhombus.WinFormsMcp`).

## How it works

This is an **MCP server plugin**, not a hooks plugin. The `.claude-plugin/plugin.json` declares an `mcpServers` entry that tells Claude Code to run `npx -y @fnrhombus/winforms-mcp` when the plugin is enabled. No hooks, no build step, no local code.

## Updating the version

When a new version of winforms-mcp is released:

1. Update the `version` field in `.claude-plugin/plugin.json` to match the latest stable release of `@fnrhombus/winforms-mcp`.
2. Commit and push to `main`.
3. Refresh the marketplace:

   ```bash
   gh workflow run update-marketplace.yml --repo fnrhombus/claude-plugins
   ```

   Or wait for the daily cron to pick it up.

## Discovery

The `claude-code-plugin` topic on this repo is what allows `fnrhombus/claude-plugins` (the central marketplace) to discover it. Don't remove the topic.
