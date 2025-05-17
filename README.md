# On a new machine
# Clone your dotfiles repo
git clone git@github.com:yourusername/dotfiles.git ~/dotfiles
cd ~/dotfiles

# Install stow
brew install stow         # macOS
sudo apt install stow     # Ubuntu

# Create symlinks
stow zsh git tmux nvim
