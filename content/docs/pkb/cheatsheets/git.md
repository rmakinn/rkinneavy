---
Title: "git"
draft: true
---

# Git Cheatsheet

## Set up machine so you don't have to type user/pwd all the time

## Turn a local directory into a Git repo

`git init`

## Clone a git repo from a URL to a local directory

`git clone https://github.com/libgit2/libgit2`

That creates a directory named libgit2, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new libgit2 directory that was just created, you’ll see the project files in there, ready to be worked on or used.

## Stage (add) a file

`git add {filename}`

### Add all markdown files

`git add *.md`

### Add all in $(cwd)

`git add .`

## Commit staged (added) files

`git commit -m "{commit message}"`

## Remote repos

### Push to

### Pull from
