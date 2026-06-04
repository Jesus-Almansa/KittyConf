# KittyConf 🐱

Personal terminal configuration files for **Kitty** terminal emulator and **Starship** prompt, running on Arch Linux (Steam Deck).

---

## Contents

| File | Description |
|------|-------------|
| `kitty.conf` | Kitty terminal emulator configuration |
| `starship.toml` | Starship cross-shell prompt configuration |

---

## Kitty (`kitty.conf`)

A customized setup for the [Kitty](https://sw.kovidgoyal.net/kitty/) GPU-accelerated terminal emulator.

**Highlights:**

- **Font:** FiraCode Nerd Font Mono at 16pt
- **Color scheme:** Warm dark theme (`#151515` background, `#c0b18b` foreground) with teal cursor (`#009688`) and red selection highlight (`#d75f5f`)
- **Cursor:** Block shape, blinking every 0.5s
- **Scrollback:** 2000 lines, paged with `less`
- **Window margin:** 15pt padding
- **Tabs:** Powerline style with slanted separators
- **Remote control:** Enabled (`allow_remote_control yes`)
- **Layouts:** All layouts enabled
- **Key bindings:** Standard Kitty mappings for clipboard, scrolling, window/tab management, and font size adjustment

---

## Starship (`starship.toml`)

A customized prompt using [Starship](https://starship.rs/), configured for a colorful segmented powerline style.

**Prompt segments (left to right):**

1. 🟣 **Username** — purple (`#9A348E`)
2. 🔴 **Directory** — pink/red (`#E91E63`), truncated to 3 levels with folder icon substitutions
3. ⬜ **Git branch & status** — light gray (`#DCDCDC`) with branch symbol
4. 🔵 **Language versions** — steel blue (`#86BBD8`), shows active runtime for: C, C++, Elixir, Elm, Go, Gradle, Haskell, Java, Julia, Maven, Node.js, Bun, Nim, Rust, Scala
5. 🟦 **Docker context** — teal (`#06969A`)
6. 🌊 **Time** — dark blue (`#33658A`) *(disabled by default)*

---

## Installation

### Kitty

```bash
# Copy config to Kitty's config directory
cp kitty.conf ~/.config/kitty/kitty.conf
```

### Starship

```bash
# Install Starship if not already installed
curl -sS https://starship.rs/install.sh | sh

# Copy config
cp starship.toml ~/.config/starship.toml

# Add to your shell's rc file (~/.bashrc, ~/.zshrc, etc.)
eval "$(starship init bash)"   # for bash
eval "$(starship init zsh)"    # for zsh
```

Make sure **FiraCode Nerd Font** is installed for proper icon rendering:

```bash
# On Arch Linux
yay -S ttf-firacode-nerd
```

---

## Requirements

- [Kitty](https://sw.kovidgoyal.net/kitty/) terminal emulator
- [Starship](https://starship.rs/) prompt
- A [Nerd Font](https://www.nerdfonts.com/) (FiraCode Nerd Font recommended)
- Arch Linux (Steam Deck or desktop)# KittyConf
