# soksak-plugin-agent-claude

A soksak plugin that adds **Claude Code** to the **Agents** category in the new-tab (+) menu.

## Behavior

At **activation (consent) time**, the plugin checks whether `claude` is installed via the
user's shell PATH. If it is not installed, the official install command is run directly in a
new terminal tab (the same command disclosed on the consent screen). Selecting the menu item
opens a terminal view and launches `claude` cleanly.

## Official Install Commands (Multi-platform)

| Platform | Command |
|---|---|
| macOS / Linux / WSL | `curl -fsSL https://claude.ai/install.sh \| bash` |
| Windows (PowerShell) | `irm https://claude.ai/install.ps1 \| iex` |

Source: [Claude Code official install docs](https://code.claude.com/docs/en/setup)

## Equivalent via Commands

```bash
sok view.open '{"program":"claude"}'
sok program.list
```

## Permissions

- `programs` — registers the program in the + menu (including automatic terminal command execution on selection)
