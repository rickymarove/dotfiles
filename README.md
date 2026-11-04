# dotfiles

My personal Fedora Linux dotfiles. A minimal, modern desktop setup focused on aesthetics, simplicity, and productivity.

Built around **Umbriel + Noctalia**, Kitty, Fish, and Starship.

## Preview

<!-- Replace these placeholders with your actual screenshots -->
<p align="center">
  <img src="assets/desktop.png" width="800" alt="Desktop preview">
</p>

<p align="center">
  <i>Desktop preview — coming soon.</i>
</p>

## Setup

| Component | Choice |
|---|---|
| OS | Fedora Linux |
| Display protocol | Wayland |
| Compositor | Umbriel |
| Desktop shell | Noctalia |
| Terminal | Kitty |
| Shell | Fish |
| Prompt | Starship |
| Terminal theme | Catppuccin Mocha |
| Terminal font | JetBrainsMono Nerd Font |
| Emoji font | Noto Color Emoji |
| Dotfile manager | GNU Stow |

## Features

- Minimal and translucent Kitty terminal.
- Catppuccin Mocha color scheme.
- JetBrainsMono Nerd Font with Nerd Font symbols.
- Noto Color Emoji support.
- Fish shell with Starship prompt.
- Umbriel window rules, transparency, and blur.
- Noctalia desktop integration.

## Repository Structure

```text
dotfiles/
├── kitty/
│   └── .config/
│       └── kitty/
│           ├── kitty.conf
│           └── current-theme.conf
│
├── fish/
│   └── .config/
│       └── fish/
│           ├── config.fish
│           └── conf.d/
│               └── starship.fish
│
├── starship/
│   └── .config/
│       └── starship.toml
│
├── umbriel/
│   └── .config/
│       └── umbriel/
│           ├── config.toml
│           └── noctalia.toml
│
├── assets/
│   └── desktop.png
│
├── packages.txt
├── .gitignore
└── README.md
```

Some configuration files, such as `noctalia.toml`, are optional.

## Installation

### 1. Install the basic packages

```bash
sudo dnf install git stow kitty fish
```

Install Starship using your preferred Fedora-compatible installation method.

Install Noto Color Emoji:

```bash
sudo dnf install google-noto-color-emoji-fonts
```

JetBrainsMono Nerd Font and the desktop components may need to be installed separately.

### 2. Clone this repository

```bash
git clone https://github.com/YOUR_USERNAME/dotfiles.git ~/Projects/dotfiles
```

```bash
cd ~/Projects/dotfiles
```

### 3. Back up existing configurations

Before creating symlinks, back up any existing configuration files that could conflict with GNU Stow.

### 4. Apply the dotfiles

```bash
stow kitty fish starship umbriel
```

Omit `umbriel` if you don't want to apply the compositor configuration.

### 5. Restart your applications

Restart Kitty, Fish, and the relevant desktop components to apply the configurations.

Validate Umbriel's configuration with:

```bash
umbriel config validate
```

## Customization

### Kitty

The Kitty configuration includes:

- Catppuccin Mocha colors.
- Transparent background.
- Minimal window decorations.
- Custom font sizing and spacing.
- Minimal tab bar.

### Fish & Starship

Fish is my interactive shell, while Starship handles the prompt.

### Umbriel & Noctalia

Umbriel handles window management, window rules, and compositor effects. Noctalia provides the desktop shell and panels.

**Note:** Display output names, monitor positions, scaling, and application shortcuts are hardware- and machine-specific. Review these settings before using the Umbriel configuration on another computer.

## Credits

- [Catppuccin](https://github.com/catppuccin)
- [Kitty Terminal](https://sw.kovidgoyal.net/kitty/)
- [Fish Shell](https://fishshell.com/)
- [Starship](https://starship.rs/)
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/)
- [Noto Fonts](https://fonts.google.com/noto)
- [Noctalia](https://noctalia.dev/)
- [GNU Stow](https://www.gnu.org/software/stow/)

## License

These are my personal configuration files. Feel free to explore, adapt, and use them as inspiration for your own setup.

---

<p align="center">
  <i>Crafted with ☕ and Linux.</i>
</p>
