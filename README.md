<h1 align="center">Delightful Starship</h1>

<p align="center">
  Rainbow powerline prompt using <a href="https://github.com/kylesnav/delightful-design-system">Delightful Design System</a> colors.
  <br>
  Based on the <a href="https://starship.rs/presets/gruvbox-rainbow">Gruvbox Rainbow</a> preset, re-themed with the Delightful palette.
</p>

---

## The Delightful Terminal Stack

| Package | Role |
|---------|------|
| [`ghostty/`](../ghostty/) | Terminal emulator — colors, fonts, keybinds |
| **`starship/`** (this package) | Prompt — rainbow powerline segments |
| [`shell/`](../shell/) | Session — tmux status bar, persistence, zsh config |
| [`iterm2/`](../iterm2/) | iTerm2 color profiles (standalone alternative) |

## Prerequisites

**Nerd Font** — the prompt uses powerline glyphs and language icons.

```sh
brew install --cask font-jetbrains-mono-nerd-font
```

## Install

1. **Install Starship** — [starship.rs](https://starship.rs)
2. **Copy config**
   ```sh
   cp starship.toml ~/.config/starship.toml
   ```
3. **Init in your shell** — add to `~/.zshrc`:
   ```sh
   eval "$(starship init zsh)"
   ```

## What's Included

The prompt displays colored powerline segments that transition left to right:

| Segment | Color | Details |
|---------|-------|---------|
| OS | Blue | macOS / Linux / Windows icon |
| Username | Blue | Always shown |
| Directory | Yellow | Truncated to 3 levels, custom folder icons for Documents, Downloads, Music, Pictures, Developer |
| Git branch | Green | Current branch name |
| Git status | Green | Modified/staged/untracked indicators |
| Language | Red | Active runtime — C, C++, Rust, Go, Node.js, PHP, Java, Kotlin, Haskell, Python |
| Docker | Pink | Docker context when active |
| Conda/Pixi | Pink | Environment name when active |

## Light Mode

A light palette variant is included as a commented block at the bottom of `starship.toml`. To use it, change `palette = 'delightful_dark'` to `palette = 'delightful_light'` and uncomment the light palette block.

## License

[MIT](LICENSE)
