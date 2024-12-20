My dot files for `~/.config` directory — nvim, tmux, alacritty etc.



# dot-files

git clone https://github.com/MaX5411/dotfiles

# Copy Alacritty config into Windows
```bash
cp $HOME/.config/alacritty/alacritty.toml \
    /mnt/c/Users/%USERNAME%/AppData/Roaming/alacritty
```

# We use Alacritty's default Linux config directory as our storage location here.
```bash
mkdir -p ~/.config/alacritty/themes
git clone https://github.com/alacritty/alacritty-theme ~/.config/alacritty/themes
```

```bash
sudo apt install -y \
    zsh git gpg pass zip unzip \    
	curl wget tmux gcc bsdmainutils htop fzf bat ripgrep build-essential
```
	
```bash
sudo ln -s $(which batcat) /usr/local/bin/bat
```

# zsh settings
# Install oh-my-zsh
# https://ohmyz.sh
# https://github.com/romkatv/powerlevel10k


````bash
cp .config/zsh/.zshrc /home/max
cp .config/zsh/.p10k.zsh /home/max
echo "source \$HOME/.config/zsh/env.zsh" >> ~/.zshrc
echo "source \$HOME/.config/zsh/aliases.zsh" >> ~/.zshrc
````


# Install nodejs and pyright LSP server for Python
# https://nodejs.org/en/download/package-manager
# choose linux and nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
export NVM_DIR="$HOME/.nvm"
nvm install 23
node -v
npm -v

npm i -g npm
npm i -g pyright

# Install typescript LSP server
npm install -g typescript-language-server typescript

# Packer for nvim
mkdir -p ~/.local/share/nvim/site/pack/packer/start/

git clone --depth 1 https://github.com/wbthomason/packer.nvim \
    ~/.local/share/nvim/site/pack/packer/start/packer.nvim

# Build telescope for nvim
cd ~/.local/share/nvim/site/pack/packer/start/telescope-fzf-native.nvim
make
```
