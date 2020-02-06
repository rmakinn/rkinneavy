---
Title: "Bashrc"
---

# `~/.shell.d`

In my `.bashrc` I tell it to source configuration options from the directory structured as below:

```
.
├── aliases
├── environment
├── functions
├── fzf
├── history
├── path
├── prompt
└── readline

```

## General 

> Why not just put it all in .bashrc?

- While it's slightly slower to source all these files, it's a bit more 'pluggable' - it's much easier for me to manage and update individual files rather than have a 300-line behemoth of a shellrc.

My environment and path are separate files so I can source my path in the `.profile` and `.bash_profile` cases and avoid pulling in certain env vars which are specifically useful for the interactive login case (i.e. `.bashrc`).

The fzf script sources bash completions and keybindings and so on.

History is literally just my shell history, I have some settings to ensure each command is stamped with unixtime, and some additional config to make sure that the history of several different simultaneous terminals is appended to the file. 
- This occasionally means I'll use ctrl+r instead of 'up' to reuse a command, and it can be inadvisable to rely on the 'include this argument from some command three commands ago' bash/readline built-in.

I specify inputrc config location (i.e. all the readline bindings and so on) as the readline file via a line in my `./environment` file.
