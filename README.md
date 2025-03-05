# My dotfiles

This directory contains the dotfiles for my system

## Requirements

Ensure you have the following installed on your system

### Git

```bash
pacman -S git
```

### Stow

```bash
pacman -S stow
```

## Installation

First, check out the dotfiles repo in your $HOME directory using git

```bash
$ git clone git@github.com/kmmenna/dotfiles.git .dotfiles
$ cd .dotfiles
```

then use GNU stow to create symlinks to the modules, like git:

```bash
$ stow git
```

or use GNU stow to create symlinks to all modules:

```bash
$ stow $(basename -a */)
```