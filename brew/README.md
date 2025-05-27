## 🛠️ Restoring on a New Machine

To re-install all your Homebrew packages:

```bash
xargs brew install < ~/brew-formulae.txt
xargs brew install --cask < ~/brew-casks.txt
```

---

## 📦 Bonus: Brew Bundle (Optional)

Alternatively, use [Brew Bundle](https://github.com/Homebrew/homebrew-bundle) for a more structured, version-controlled setup.

To generate a Brewfile:

```bash
brew bundle dump --describe --file=~/.dotfiles/brew/Brewfile
```

To restore everything from your Brewfile:

```bash
brew bundle --file=~/.dotfiles/brew/Brewfile
```

This method includes taps, formulae, and casks in a single file.
