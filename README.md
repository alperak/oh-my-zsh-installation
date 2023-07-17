### Necessary packages for zsh & terminator
sudo apt-get install python git curl wget -y
### Install Terminator
sudo apt-get install terminator -y
### For Ubuntu zsh
sudo apt-get install zsh
### Change zsh as the default shell
chsh -s $(which zsh)
### Install Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
### Powerlevel10k is a theme for zsh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
### Install fonts for Powerlevel10k.
sudo apt-get install fonts-powerline
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/Meslo.zip &&
unzip Meslo.zip -d Meslo && sudo cp -r Meslo /usr/share/fonts
### Set Zsh theme
nano ~/.zshrc
Set ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc.
### Change terminal font to MesloLGS Nerd Font Regular
### Configure the terminal
"source ~/.zshrc" or "p10k configure" or reopen terminal.
# Install Plugins
### Auto Suggestions
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
### Syntax Higlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
### Autojump
git clone https://github.com/wting/autojump.git
cd autojump && python3 ./install.py
(also dont forget to add terminal output to bashrc file.)
### Add plugins
nano ~/.zshrc
find "plugins=" line and update like this:
plugins=(git zsh-autosuggestions zsh-syntax-highlighting autojump)
### Load to configuration
source ~/.zshrc
### Install dark theme for Terminator
git clone https://github.com/dracula/terminator.git
cd terminator && ./install.sh
### Change terminal font to MesloLGS Nerd Font Regular
### For more plugins, you can check Oh-My-Zsh's github page
https://github.com/ohmyzsh/ohmyzsh
