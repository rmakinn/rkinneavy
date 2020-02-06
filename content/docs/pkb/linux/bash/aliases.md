---
Title: "Aliases"
---

# Aliases

> Below are some notable aliases. I do remember to use most of these. Sometimes.

```bash

# read in any changes made to the config since the terminal instance began
alias shrc='source ~/.bashrc'

# run the last command as root
alias pls='sudo !! '

# append the last run command to a notes file in the $cwd
alias n="history | tail -2 | head -1 | tr -s ' ' | cut -d' ' -f3- | awk '{print \"# \"\$0}' >> notes"

# not mine - I wish! Imaginative, I'd like to think of more like this
alias map='xargs -n1'

## filesystem
alias ..='cd -- ..'
alias ...='cd -- ../..'
alias ....='cd -- ../../..'

alias mkd='mkdir' # save 2 keystrokes
alias mkp='mkdir -p' # make parent dirs if needed

alias ls='exa'
alias sl='exa' # in case of oopsie

alias la='exa -a'  # all files and dirs
alias ll='exa -al' # all + long
alias lt='exa -aT -L 2' # all + tree listing

## pkg
alias xi='sudo xbps-install -S'
alias xu='sudo xbps-install -Syuv'
alias xr='sudo xbps-remove'
alias xs='xbps-query -Rs'
alias xm='sudo xbps-query -m'

## git
alias ga='git add '
alias gad='git add .'
alias gc='git clone'
alias gcm='git commit -m '
alias gpom='git push origin master'
alias gsa='git submodule add '

## misc
alias yt='youtube-dl --config-location ~/.config/youtube-dl/video'
alias ytm='youtube-dl --config-location ~/.config/youtube-dl/audio'
alias wget='wget --hsts-file ~/.config/wget/hsts' # keep your $HOME tidy

alias today='pdd | tee >(xclip -sel clip)'
alias myip='curl icanhazip.com'
alias x='atool -x'

```
