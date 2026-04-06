# delightful-starship

Starship prompt theme — rainbow powerline with Delightful colors.

## Source of Truth

Token hex values come from [delightful-design-system](https://github.com/kylesnav/delightful-design-system). Hex values are hardcoded in the TOML palette block.

## Key Files

- `starship.toml` — Complete Starship config. Palette block + prompt segment definitions.

## Conventions

- Based on the Gruvbox Rainbow preset. Palette variable names are inherited Gruvbox slots — they DON'T match Delightful color families:
  - `color_blue` = Cyan (`#5cb8d6`)
  - `color_orange` = Pink (`#ff4fa8`)
  - `color_purple` = Pink (`#ff4fa8`)
  - `color_aqua` / `color_green` = Green (`#3aad5f`)
- Light variant is commented out at the bottom of the file. Switch by changing `palette = 'delightful_light'`.
- Requires a Nerd Font for powerline glyphs.
