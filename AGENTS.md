# delightful-starship

Starship prompt theme based on Gruvbox Rainbow and rethemed with Delightful colors.

## Source of Truth

`starship.toml` is the source of truth for this repo. Hex values are a hardcoded snapshot from [delightful.build](https://delightful.build/).

## Validate

```sh
STARSHIP_CONFIG="$PWD/starship.toml" starship explain >/tmp/delightful-starship-explain.txt
```

Also inspect the commented light palette when changing any dark palette value.

## Editing Rules

- Keep inherited Gruvbox slot names documented when they do not match Delightful color families.
- Do not rename palette variables unless the Starship format and README are updated together.
- Requires a Nerd Font for prompt glyphs; note this in user-facing docs.

## Screenshots

Screenshots should show a real shell prompt with enough context to exercise directory, git, runtime, and time segments. Use Ghostty or iTerm2 with the matching Delightful terminal palette.
