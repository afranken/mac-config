#ZSH

This folder contains zsh configuration.

The files here are tested with [oh-my-zsh](http://ohmyz.sh/), and may not work with "regular" zsh installations.

[Nerd-Font](https://github.com/bhilburn/powerlevel9k/wiki/Install-Instructions#option-4-install-nerd-fonts) is already installed if `brew-cask-install.sh` was executed, configure iTerm to use it.

* `zsh-bootstrap.sh` : link `.profile` to `~/.profile`
* `.profile` : this file is loaded by every interactive shell when linked to `~/.profile`.
* Edit `~/.zshrc` (unfortunately this can't be automated or outsourced to a separate file) 
    * Add ZSH Theme config:
        ```
        #ZSH_THEME="robbyrussell"
           
        # See
        # https://github.com/bhilburn/powerlevel9k/wiki/Stylizing-Your-Prompt
        ZSH_THEME="powerlevel9k/powerlevel9k"
        POWERLEVEL9K_MODE="nerdfont-complete"
        POWERLEVEL9K_COLOR_SCHEME='light'
        POWERLEVEL9K_PROMPT_ON_NEWLINE=true
        POWERLEVEL9K_RPROMPT_ON_NEWLINE=true
        #POWERLEVEL9K_SHORTEN_DIR_LENGTH=5
        #POWERLEVEL9K_SHORTEN_STRATEGY="truncate_with_package_name"
        POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(status time dir vcs)
        POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=()
        POWERLEVEL9K_CHANGESET_HASH_LENGTH=8
        ```
    * Enable plugins for command completion:
        `plugins=(git mvn docker)`
    * Source custom `.zshrc`:
        * `. ~/.dotfiles/oh-my-zsh/.zshrc`