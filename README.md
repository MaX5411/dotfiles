My dot files for `~/.config` directory — nvim, tmux, alacritty etc.



# dot-files

`git clone https://github.com/MaX5411/dotfiles .config`

# Copy Alacritty config into Windows
```bash
cp $HOME/.config/alacritty/alacritty.toml \
    /mnt/c/Users/%USERNAME%/AppData/Roaming/alacritty
```

# Alacritty's themes
```bash
mkdir -p ~/.config/alacritty/themes
git clone https://github.com/alacritty/alacritty-theme ~/.config/alacritty/themes
```

# Install standart utils
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
https://ohmyz.sh

https://github.com/romkatv/powerlevel10k


````bash
cp .config/zsh/.zshrc /home/max
cp .config/zsh/.p10k.zsh /home/max
echo "source \$HOME/.config/zsh/env.zsh" >> ~/.zshrc
echo "source \$HOME/.config/zsh/aliases.zsh" >> ~/.zshrc
````



