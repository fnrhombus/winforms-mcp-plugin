# winforms-mcp

**Give Claude Code full control of Windows desktop apps — click buttons, fill forms, read tables, take screenshots — all headless.**

[![NuGet](https://img.shields.io/nuget/v/Rhombus.WinFormsMcp)](https://www.nuget.org/packages/Rhombus.WinFormsMcp)
[![npm](https://img.shields.io/npm/v/@fnrhombus/winforms-mcp)](https://www.npmjs.com/package/@fnrhombus/winforms-mcp)
[![license](https://img.shields.io/github/license/fnrhombus/winforms-mcp)](./LICENSE)

## The problem

Claude Code can't interact with Windows desktop applications. If you need to automate a WinForms app — launch it, click through dialogs, scrape data from grids, validate UI state — you're on your own.

## The fix

This plugin adds a WinForms automation MCP server that gives Claude 33 tools for headless UI automation via [FlaUI](https://github.com/FlaUI/FlaUI):

- **Launch & attach** to Windows processes
- **Find & interact** with UI elements (click, type, select, drag-drop)
- **Read** properties, table data, tooltips, clipboard
- **Wait** for elements and conditions
- **Screenshot** windows — even on a hidden desktop
- **Headless mode** — run automations without showing any windows

## Install

```
/plugin marketplace add fnrhombus/claude-plugins
/plugin install winforms-mcp@fnrhombus-plugins
```

Full documentation and source: [fnrhombus/winforms-mcp](https://github.com/fnrhombus/winforms-mcp)

## Support

- **[GitHub Sponsors](https://github.com/sponsors/fnrhombus)**
- **[Buy Me a Coffee](https://buymeacoffee.com/fnrhombus)**

## License

MIT
