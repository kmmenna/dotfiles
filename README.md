# My dotfiles

Dotfiles managed with [Chezmoi](https://chezmoi.io).

## Contents

- **Shell:** zsh (`.zshenv`, `.zshrc`)
- **Git:** `.gitconfig`
- **Tmux:** `.tmux.conf`, `~/.config/tmux/` (config, theme; TPM plugins via external)
- **Oh My Posh:** `~/.config/ohmyposh/posh.toml`

## Requirements

- [Git](https://git-scm.com/)
- [Chezmoi](https://chezmoi.io/)

### Install Chezmoi

**One-liner (curl):**
```bash
sh -c "$(curl -fsLS get.chezmoi.io)"
```

**Package manager (examples):**
```bash
# Fedora / RHEL
sudo dnf install chezmoi

# Arch
sudo pacman -S chezmoi
```

## Installation

Clone the repo and apply with Chezmoi:

```bash
chezmoi init https://github.com/kmmenna/dotfiles.git
chezmoi apply
```

Or, if you already have the repo cloned:

```bash
chezmoi init /path/to/dotfiles
chezmoi apply
```

To see what would change without applying:

```bash
chezmoi diff
```

## Externals

- **TPM (Tmux Plugin Manager)** is fetched by Chezmoi from GitHub (see `.chezmoiexternal.toml`). After the first apply, run `prefix + I` in tmux to install plugins.

## Daily use

- Edit a managed file: `chezmoi edit ~/.zshrc`
- Add a new file: `chezmoi add ~/.path/to/file`
- Preview changes: `chezmoi diff`
- Apply changes: `chezmoi apply`
- Pull and apply updates: `chezmoi update`
