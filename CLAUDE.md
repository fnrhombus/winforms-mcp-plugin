# winforms-mcp-plugin

Claude Code plugin manifest for the [winforms-mcp](https://github.com/fnrhombus/winforms-mcp) MCP server. This repo contains only the plugin metadata — the actual server is distributed via npm (`@fnrhombus/winforms-mcp`) and NuGet (`Rhombus.WinFormsMcp`).

## How it works

This is an **MCP server plugin**, not a hooks plugin. The `.claude-plugin/plugin.json` declares an `mcpServers` entry that tells Claude Code to run `npx -y @fnrhombus/winforms-mcp` when the plugin is enabled. No hooks, no build step, no local code.

## Why nothing auto-updates

The `mcpServers` entry uses `npx -y @fnrhombus/winforms-mcp`, which always fetches the latest version from npm at runtime. There's nothing to version-bump here on release — the plugin repo is effectively static infrastructure.

## README sync

The README in this repo mirrors the source repo's README, but with **plugin install instructions** instead of raw MCP config. This is **not automated** — when the source repo's README changes, this repo's README must be updated manually to match.

**When updating:** copy the source README, then replace the "Quick start" section (MCP JSON config) with the plugin install command (`/plugin install winforms-mcp@fnrhombus-plugins`). Also update any relative doc links to absolute URLs pointing to the source repo. See the current README for the pattern.

## Discovery

The `claude-code-plugin` topic on this repo is what allows `fnrhombus/claude-plugins` (the central marketplace) to discover it. Don't remove the topic.
