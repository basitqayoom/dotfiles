# 🗂️ Dotfiles Setup using GNU Stow

This repository contains my personal dotfiles managed using [GNU Stow](https://www.gnu.org/software/stow/). This setup allows you to quickly configure a new system with my preferred environment, including Zsh, Git, Tmux, and Neovim.

---

## 📦 What’s Included

- **zsh** - `.zshrc`, `.zprofile`, and Powerlevel10k theme configuration.
- **git** - `.gitconfig`.
- **tmux** - `.tmux.conf`.
- **nvim** - Neovim configuration files under `.config/nvim`.

---

## 🆕 Adding Files to Dotfiles for the First Time

To start tracking your configuration files with this dotfiles repo:

1. **Create a Directory for Each App**

    For each tool (e.g., zsh, git), create a directory inside your dotfiles repo:

    ```bash
    mkdir -p ~/dotfiles/zsh
    mkdir -p ~/dotfiles/git
    mkdir -p ~/dotfiles/tmux
    mkdir -p ~/dotfiles/nvim/.config/nvim
    ```

2. **Move Your Existing Config Files**

    Move your config files into the corresponding directories. For example:

    ```bash
    mv ~/.zshrc ~/dotfiles/zsh/
    mv ~/.zprofile ~/dotfiles/zsh/
    mv ~/.p10k.zsh ~/dotfiles/zsh/
    mv ~/.gitconfig ~/dotfiles/git/
    mv ~/.tmux.conf ~/dotfiles/tmux/
    mv -r ~/.config/nvim/* ~/dotfiles/nvim/.config/nvim/
    ```

    > **Tip:** Backup your configs before moving.

3. **Symlink with Stow**

    From your dotfiles directory, run:

    ```bash
    cd ~/dotfiles
    stow zsh
    stow git
    stow tmux
    stow nvim
    ```

    This will symlink the files back to their original locations.

---

## 💻 Setting Up Dotfiles on a New Machine

1. **Install Git and Stow**

    ```bash
    # Debian/Ubuntu
    sudo apt update
    sudo apt install git stow

    # macOS
    brew install git stow
    ```

2. **Clone the Repository**

    ```bash
    git clone git@github.com:yourusername/dotfiles.git ~/dotfiles
    cd ~/dotfiles
    ```

    > Replace `yourusername` with your GitHub username.

3. **Symlink Your Configurations**

    ```bash
    stow zsh
    stow git
    stow tmux
    stow nvim
    ```

    Your dotfiles are now active on the new machine.

---

## ✏️ Editing Config Files and Committing Changes

1. **Edit Your Config Files**

    Open and edit any config file inside the dotfiles repo. For example:

    ```bash
    nvim ~/dotfiles/zsh/.zshrc
    ```

2. **Check the Changes**

    ```bash
    cd ~/dotfiles
    git status
    ```

3. **Stage and Commit**

    ```bash
    git add zsh/.zshrc
    git commit -m "Update .zshrc with new aliases"
    ```

4. **Push to GitHub**

    ```bash
    git push origin main
    ```

    > Replace `main` with your branch name if different.

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
