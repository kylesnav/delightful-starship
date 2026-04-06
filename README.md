# Delightful for Starship

Rainbow powerline prompt themed with the [Delightful](https://github.com/kylesnav/delightful-design-system) color palette. Based on the [Gruvbox Rainbow](https://starship.rs/presets/gruvbox-rainbow) preset, re-themed with Delightful's warm, neo-brutalist colors.

<!-- TODO: Add screenshot of prompt in terminal -->

## Prerequisites

- [Starship](https://starship.rs) installed
- A [Nerd Font](https://www.nerdfonts.com/) for powerline glyphs and language icons (e.g. `brew install --cask font-jetbrains-mono-nerd-font`)

## Install

1. Copy the config into place:
   ```sh
   cp starship.toml ~/.config/starship.toml
   ```
2. Add Starship init to your shell (e.g. `~/.zshrc`):
   ```sh
   eval "$(starship init zsh)"
   ```

## What's Configured

The prompt renders colored powerline segments flowing left to right:

| Segment | Palette Color | Details |
|---------|---------------|---------|
| OS icon | Pink (`color_orange`) | macOS, Linux, Windows, and distro-specific icons |
| Username | Pink (`color_orange`) | Always shown |
| Directory | Yellow (`color_yellow`) | Truncated to 3 levels; custom icons for Documents, Downloads, Music, Pictures, Developer |
| Git branch | Green (`color_aqua`) | Branch name with icon |
| Git status | Green (`color_aqua`) | Modified / staged / untracked indicators |
| Languages | Cyan (`color_blue`) | Active runtime -- C, C++, Rust, Go, Node.js, PHP, Java, Kotlin, Haskell, Python |
| Docker | Gray (`color_bg3`) | Docker context when active |
| Conda / Pixi | Gray (`color_bg3`) | Environment name when active |
| Time | Dark (`color_bg1`) | Current time (HH:MM) |

A second prompt line shows a Nerd Font glyph: green on success, red on error, with vim-mode variants.

## Palette

The `delightful_dark` palette maps Starship color names to Delightful hex values:

| Name | Hex | Delightful Family |
|------|-----|-------------------|
| `color_fg0` | `#eee9e3` | Neutral (foreground) |
| `color_bg1` | `#3c3632` | Neutral (dark surface) |
| `color_bg3` | `#615d58` | Neutral (mid surface) |
| `color_blue` | `#5cb8d6` | Cyan |
| `color_aqua` | `#3aad5f` | Green |
| `color_green` | `#3aad5f` | Green (alias) |
| `color_orange` | `#ff4fa8` | Pink |
| `color_purple` | `#ff4fa8` | Pink (alias) |
| `color_red` | `#e8554c` | Red |
| `color_yellow` | `#f5c526` | Yellow |

> **Note:** The slot names come from the Gruvbox Rainbow preset and don't always match Delightful's color families. `color_blue` is actually Cyan, `color_orange`/`color_purple` both map to Pink, and `color_aqua`/`color_green` both map to Green.

### Light Mode

A light palette variant is included as a commented block at the bottom of `starship.toml`. To switch:

1. Change `palette = 'delightful_dark'` to `palette = 'delightful_light'`
2. Uncomment the `[palettes.delightful_light]` block at the end of the file

## Part of Delightful

This is one piece of the Delightful terminal stack:

| Package | Role |
|---------|------|
| [delightful-ghostty](https://github.com/kylesnav/delightful-ghostty) | Terminal emulator -- colors, fonts, keybinds |
| **delightful-starship** | Prompt -- rainbow powerline segments |
| [delightful-shell](https://github.com/kylesnav/delightful-shell) | Shell session -- tmux, zsh config |
| [delightful-iterm2](https://github.com/kylesnav/delightful-iterm2) | iTerm2 color profiles |

All packages share the same [Delightful Design System](https://github.com/kylesnav/delightful-design-system) palette.

## License

[MIT](LICENSE)
