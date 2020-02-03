---
Title: "Dotfiles"
Tags:
- stub
- dots
---

## management

- git --bare repo method as detailed in atlassian tutorial and similar
  - although I have a clever 'dots' alias
- I tried yadm, stow etc but they never really clicked, needed to do it this way to grok it
  - I don't want to put a file in the git repo and then symlink it out. I want the file to be in the right place, and simply track it by adding it to the bare git repo.

## organisation

- In general, if I can specify a location for a config file it's gonna get placed in `~/.config` 
  - generally you have to do this with environmental variables, the worst case involves passing something like `-c /path/to/.config/dir` and aliasing that to the plain command.
- I make good use of `~/.local` as this is where user-specific configuration and binaries ought to go, imo - put fonts, icons, themes in the share subdirectory, and scripts and AppImages etc in bin.
