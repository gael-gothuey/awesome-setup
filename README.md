# wsl-setup

- Install zsh and python3-pygments (a generic syntax highlighter suitable) packages
sudo apt-get install zsh python3-pygments

- sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools
/install.sh -O -)"

-Useful plugins

git clone https://github.com/zsh-users/zsh-autosuggestions.git 
$ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git 
$ZSH_CUSTOM/plugins/zsh-syntax-highlighting

- list of cool plugins
plugins=(git ssh-agent docker docker-compose oc kubectl terraform zshautosuggestions zsh-syntax-highlighting colorize ubuntu)
- reload 

source ~/.zshrc
