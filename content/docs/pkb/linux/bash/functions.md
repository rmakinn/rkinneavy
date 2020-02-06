---
Title: "Functions"
---

# Bash Functions

I really love bash functions. I scoured the web for awesome ones, and wrote a few of my own. Here are a few worthy of mention:

TODO: explanatory comments

## Brain-assisters

```bash

cheats() {
    cheat -l | sk --preview "cheat {1}"
}

explain () {
    if [ "$#" -eq 0 ]; then
      while read  -p "Command: " cmd; do
        curl -Gs "https://www.mankier.com/api/v2/explain/?cols="$(tput cols) --data-urlencode "q=$cmd"
      done
      echo "Bye!"
    elif [ "$#" -eq 1 ]; then
      curl -Gs "https://www.mankier.com/api/v2/explain/?cols="$(tput cols) --data-urlencode "q=$1"
    else
      echo "Usage"
      echo "explain                  interactive mode."
      echo "explain 'cmd -o | ...'   one quoted command to explain it."
    fi
}

manflags() {
    man "$1" | awk '{$1=$1;print}' | grep "^\-"
}

tldrw() {
   w3m -dump "https://raw.githubusercontent.com/tldr-pages/tldr/master/pages/common/$1.md"
   w3m -dump "https://raw.githubusercontent.com/tldr-pages/tldr/master/pages/linux/$1.md"
}

halp() {
    (tldr $1 ; man $1) | cat | less
}

```

## Fuzzy-finder

```bash

fzp() {
    fzf --preview 'bat {}'
}

fif() {
    if [ ! "$#" -gt 0 ]; then echo "Need a string to search for!"; return 1; fi
    local file
    file="$(rga --max-count=1 --ignore-case --files-with-matches --no-messages "$@" | fzf-tmux +m --preview="rga --ignore-case --pretty --context 10 '"$@"' {}")" && open "$file"
}

fzd() {
    local dir
    dir=$(fd -H -t d -E yarn -E node -E node_modules | fzf --border +m);
    cd "$dir" && ls
}

fxi() {
    xbps-query -Rs "" | cut --delimiter " " --fields 1-2 | fzf -m --preview 'xbps-query -R {2}' | cut --delimiter " " --fields 2 | xargs -ro sudo xbps-install
}

fxr() {
    xbps-query -l | cut --delimiter " " --fields 1-2 | fzf -m --preview 'xbps-query -R {2}' | cut --delimiter " " --fields 2 | xargs -ro sudo xbps-remove
}

```

## Misc Utility

```bash

open() {
    mimeo "$1" &> /dev/null &
}


weather() {
    curl wttr.in/sheffield;
}

mkcd() {
    mkdir -p "$@" && cd "$_" && ls
}

cl() {
    last_dir="$(ls -Frt | grep '/$' | tail -n1)"
    if [ -d "$last_dir" ]; then
            cd "$last_dir"
    fi
}

# open the current path or file in GitHub
gho() {
	local file=$1
	local remote=${2:-origin}

	# get the git root dir, branch, and remote URL
	local gr=$(git rev-parse --show-toplevel)
	local branch=$(git rev-parse --abbrev-ref HEAD)
	local url=$(git config --get "remote.$remote.url")

	[[ -n $gr && -n $branch && -n $remote ]] || return 1

	# construct the path
	local path=${PWD/#$gr/}
	[[ -n $file ]] && path+=/$file

	# extract the username and repo name
	local a
	IFS=:/ read -a a <<< "$url"
	local len=${#a[@]}
	local user=${a[len-2]}
	local repo=${a[len-1]%.git}

	local url="https://github.com/$user/$repo/tree/$branch$path"
	echo "$url"
	open "$url"
}

```
