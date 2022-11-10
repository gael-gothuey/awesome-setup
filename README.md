# Set up bash

## Set up Oh-my-zsh

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

## Useful plugins

**Syntax highlighting & auto-suggestion**

```bash
# Install zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
# Install zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

**McFly (Fly through your shell history)**

```bash
curl -LSfs https://raw.githubusercontent.com/cantino/mcfly/master/ci/install.sh | sh -s -- --git cantino/mcfly
```

Add the following to the end of `~/.zshrc`

```bash
eval "$(mcfly init zsh)"
```

Edit ~/.zshrc  and add cool plugins

```bash
# Update plugins
vim ~/.zshrc
# Add this list of useful plugins 
plugins=(git ssh-agent docker docker-compose oc kubectl terraform zsh-autosuggestions zsh-syntax-highlighting colorize ubuntu)
```

Save and apply changes

```bash
source ~/.zshrc 
or
code ~/.zshrc
```

Set a theme to your bash (or leave it with default value)

```bash
vim ~/.zshrc
ZSH_THEME="amuse"
```

### File ~/.zshrc result

```bash
export ZSH="$HOME/.oh-my-zsh"
ZSH_THEME="amuse"
# zstyle ':omz:update' mode reminder  # just remind me to update when it's time
ENABLE_CORRECTION="true"
plugins=(git ssh-agent docker docker-compose oc kubectl terraform zsh-autosuggestions zsh-syntax-highlighting colorize ubuntu)
source $ZSH/oh-my-zsh.sh

# User configuration
eval "$(mcfly init zsh)"
```

## Set up Windows Terminal

> Other theme: <https://windowsterminalthemes.dev/>

add `One Half Dark` theme in `settings.json` (Latest version of Windows Terminal already has One Half Dark theme)

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
download [JetBrains Nerd Font](https://github.com/ryanoasis/nerd-fonts/blob/master/patched-fonts/JetBrainsMono/Ligatures/Regular/complete/JetBrains%20Mono%20Regular%20Nerd%20Font%20Complete.ttf)
Then set font in <distro> -> appearance -> theme -> One Half Dark 
Then set font in <distro> -> appearance -> font -> select JetBrains Mono 
```

## Set up VSCode

Add bracket pair colorization

1. Open Settings

2. find ``Pair``

3. Set True bracketPairs

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

Add custom shortcuts (switch to prompt terminal):

```json
// Place your key bindings in this file to override the defaults
[
// Toggle between terminal and editor focus
{ "key": "ctrl+[IntlBackslash]", "command": "workbench.action.terminal.focus"},
]
```

# Useful VSCode plugins

- TODO Highlight <https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight>
- Code Spell Checker <https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker>
- Trailing Spaces <https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces>
- Emoji Log <https://marketplace.visualstudio.com/items?itemName=ahmadawais.emoji-log-vscode>
- Git supercharged <https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens>
- Live Share <https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare>
- Markdown All in One <https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one>
- REST Client <https://marketplace.visualstudio.com/items?itemName=humao.rest-client>

## Debian/Ubuntu set up

TODO