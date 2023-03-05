## zsh terminal in windows
#Steps to make zsh in windows

1.  Enable Virtualization
2.  Install Linux subsystem
3.  Install ubuntu app & terminal from microsoft apps

#Run below commands on linux system


```
sudo apt update

sudo apt install zsh -y

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

```
#Download mononoki fonts from nerdfonts https://www.nerdfonts.com/font-downloads
    extract and install one by one and then

_Install code in windows not on subsystem_

```
code ~/.zshrc
```

change ZSH_THEME="spaceship" and all below line to the last

```
SPACESHIP_PROMPT_ADD_NEWLINE="true"

SPACESHIP_CHAR_SYMBOL=" \uf0e7 "

#SPACESHIP_CHAR_PREFIX="\uf296"

SPACESHIP_CHAR_SUFFIX=(" ")

SPACESHIP_CHAR_COLOR_SUCCESS="yellow"

SPACESHIP_PROMPT_DEFAULT_PREFIX="$USER"

SPACESHIP_PROMPT_FIRST_PREFIX_SHOW="true"

SPACESHIP_USER_SHOW="true"

export LS_COLORS="di=34;40:ln=36;40:so=35;40:pi=33;40:ex=32;40:bd=1;33;40:cd=1;33;40:su=0;41:sg=0;43:tw=0;42:ow=34;40:"

zstyle ':completion:*:default' list-colors ${(s.:.)LS_COLORS}

```

`source ~/.zshrc`

8. Go To terminal -> Go to Settings -> Open json file and add windows-settings.json content


# Oh my zsh.

## Install ZSH.

```
sudo apt install zsh-autosuggestions zsh-syntax-highlighting zsh
```

## Install Oh my ZSH.
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install plugins.
 - autosuggesions plugin
 
	`git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
	
 - zsh-syntax-highlighting plugin
 
	`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`
	
 - zsh-fast-syntax-highlighting plugin
 
	`git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting`
	
 - zsh-autocomplete plugin
	
	`git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete`
	
## Enable plugins by adding them to .zshrc.
 - Open .zshrc
	
	`code ~/.zshrc`
	
 -  Find the line which says `plugins=(git)`.
	
 -  Replace that line with
	`plugins=(git zsh-autosuggestions zsh-syntax-highlighting fast-syntax-highlighting zsh-autocomplete)`
	
## References

 - [Oh my ZSH](https://github.com/ohmyzsh/ohmyzsh)
 - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
 - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
 - [zsh-fast-syntax-highlighting](https://github.com/zdharma/fast-syntax-highlighting)
 - [zsh-autocomplete](https://github.com/marlonrichert/zsh-autocomplete)

