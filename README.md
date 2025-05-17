# 🗂️ Dotfiles Setup using GNU Stow

This repository contains my personal dotfiles managed using [GNU Stow](https://www.gnu.org/software/stow/). This setup allows you to quickly configure a new system with my preferred environment, including Zsh, Git, Tmux, and Neovim.

---

## 📦 What’s Included

- **zsh** - `.zshrc`, `.zprofile`, and Powerlevel10k theme configuration.
- **git** - `.gitconfig`.
- **tmux** - `.tmux.conf`.
- **nvim** - Neovim configuration files under `.config/nvim`.

---

---

## 💻 Setting Up on a New Machine

To set up your environment on a new system:

### 1. Install Git and Stow

```bash
# Debian/Ubuntu
sudo apt update
sudo apt install git stow

# macOS
brew install git stow
```

### 2. Clone the Repository

```bash
git clone git@github.com:yourusername/dotfiles.git ~/dotfiles
cd ~/dotfiles
```

> Replace `yourusername` with your GitHub username.

### 3. Stow Your Configurations

```bash
stow zsh
stow git
stow tmux
stow nvim
```

That's it! Your dotfiles are now symlinked into the appropriate places in your home directory.

----


## ⚙️ Installation

### 1. Install `stow`

#### On macOS (Homebrew)
```bash
brew install stow
```

#### On Debian/Ubuntu
```bash
sudo apt update
sudo apt install stow
```

---

### 2. Clone This Repository

```bash
git clone git@github.com:yourusername/dotfiles.git ~/dotfiles
cd ~/dotfiles
```

> Replace `yourusername` with your actual GitHub username.

---

### 3. Use `stow` to Set Up Symlinks

Run the following to symlink each configuration set into your `$HOME` directory:

```bash
stow zsh
stow git
stow tmux
stow nvim
```

This will create symbolic links such as:

- `~/.zshrc → ~/dotfiles/zsh/.zshrc`
- `~/.gitconfig → ~/dotfiles/git/.gitconfig`

---

## 🧹 Unlinking (Unstow)

If you want to remove symlinks:

```bash
stow -D zsh
```

---

## 🛡️ .gitignore (Recommended)

This repository excludes sensitive or junk files. Here's a recommended `.gitignore`:

```gitignore
.cache/
.zsh_history
.zcompdump*
.Trash/
.DS_Store
.viminfo
.lesshst
```

---

## 📁 Folder Structure

```
dotfiles/
├── zsh/
│   ├── .zshrc
│   ├── .zprofile
│   └── .p10k.zsh
├── git/
│   └── .gitconfig
├── tmux/
│   └── .tmux.conf
├── nvim/
│   └── .config/
│       └── nvim/
```

---

## ✨ Optional Enhancements

- Add a `bootstrap.sh` script to automate setup
- Install `oh-my-zsh` via script
- Add configs for other tools like `starship`, `bat`, `htop`, etc.

---

## 🤝 Contributing

This setup is personal, but feel free to fork and adapt it to your own needs!

---
