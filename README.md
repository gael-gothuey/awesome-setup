# Set up bash

## Set Oh-my-zsh

Install zsh

```bash
sudo apt install zsh
```

install Oh-My-Bash

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

Install zsh and python3-pygments (a generic syntax highlighter suitable) packages

```bash
sudo apt-get install zsh python3-pygments
```

Useful plugins

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

Edit ~/.zshrc  and add cool plugins

```bash
vim ~/.zshrc
edit plugins --> plugins=(git ssh-agent docker docker-compose oc kubectl terraform zsh�autosuggestions zsh-syntax-highlighting colorize ubuntu)
```

Save and apply changes

```bash
source ~/.zshrc 
```

Set a theme to your bash (or leave it with default value) 

```bash
vim ~/.zshrc
ZSH_THEME="amuse"
```

## Set up Windows Terminal

add ``One Half Dark`` theme in ``settings.json``

```json
        {
            "name": "One Half Dark",
            "background": "#282C34",
            "black": "#282C34",
            "blue": "#61AFEF",
            "brightBlack": "#5A6374",
            "brightBlue": "#61AFEF",
            "brightCyan": "#56B6C2",
            "brightGreen": "#98C379",
            "brightPurple": "#C678DD",
            "brightRed": "#E06C75",
            "brightWhite": "#DCDFE4",
            "brightYellow": "#E5C07B",
            "cursorColor": "#FFFFFF",
            "cyan": "#56B6C2",
            "foreground": "#DCDFE4",
            "green": "#98C379",
            "purple": "#C678DD",
            "red": "#E06C75",
            "selectionBackground": "#FFFFFF",
            "white": "#DCDFE4",
            "yellow": "#E5C07B"
        },
```

Set  ``One Half Dark`` and  ``Jetbrains Mono font`` 

```bash
download : https://www.jetbrains.com/fr-fr/lp/mono/
Then set font in <distro> -> apparence -> theme -> One Half Dark 
Then set font in <distro> -> apparence -> font -> select JetBrains Mono 
```

## Set up VSCode

Add bracket pair colorization

1. Open Settings

2. find ``Pair`` 

3. Tick :ballot_box_with_check: bracketPairColorization

4. Set True bracketPairs

Install ``Atom One Dark Theme`` : [Atom One Dark Theme - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)

Add custom configuration : 

```json
{
    "security.workspace.trust.untrustedFiles": "open",
    "editor.bracketPairColorization.enabled": true,
    "editor.guides.bracketPairs": true,
    "workbench.colorTheme": "Atom One Dark",
    "editor.fontFamily": "JetBrains Mono,Consolas, 'Courier New', monospace",
    "editor.fontSize": 13,
    "editor.fontWeight": "300",
    "editor.fontLigatures": true,
    "workbench.colorCustomizations" : {
        //https://glitchbone.github.io/vscode-base16-term/#/gruvbox-dark-soft
        "terminal.background":"#35364d",
    },
} 
```
# Useful VSCode plugins
- Name: TODO Highlight
Id: wayou.vscode-todo-highlight
Description: highlight TODOs, FIXMEs, and any keywords, annotations...
Version: 1.0.5
Publisher: Wayou Liu
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight

