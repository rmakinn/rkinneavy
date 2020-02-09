---
Title: "git"
draft: true
---

# Git Cheatsheet

Lots copied verbatim from here: https://git-scm.com/book

Also see: https://github.github.com/training-kit/downloads/github-git-cheat-sheet/

## Set up machine so you don't have to type user/pwd all the time

### Cache for n seconds

`git config --global credential.helper 'cache --timeout=3600'`

### Setup SSH

[Step 0 - remind yourself about SSH](https://help.github.com/en/enterprise/2.18/user/github/authenticating-to-github/about-ssh)

[Step 1 - generate new SSH key and add to ssh-agent](https://help.github.com/en/enterprise/2.18/user/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

[Step 2 - add new ssh key to your GitHub account](https://help.github.com/en/enterprise/2.18/user/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

URL: https://github.com/settings/keys

[Step 2.1 - add a passphrase if you didn't already](https://help.github.com/en/enterprise/2.18/user/github/authenticating-to-github/working-with-ssh-key-passphrases)

## Turn a local directory into a Git repo

`git init`

Creates a new subdirectory named .git that contains all of your necessary repository files — a Git repository skeleton.

## Clone a git repo from a URL to a local directory

`git clone https://github.com/libgit2/libgit2`

That creates a directory named libgit2, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new libgit2 directory that was just created, you’ll see the project files in there, ready to be worked on or used.

## Add a file

`git add {filename}`

A multipurpose command — you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content to the next commit” rather than “add this file to the project”.

### Add all markdown files

`git add *.md`

### Add all in $(cwd)

`git add .`

Recall Git stages a file exactly as it is when you run the `git add` command. So if you modify a staged file and call `git status`, you'll see both a staged and an unstaged version.

## View (un)staged changes ready to commit

`git status`

Pass `-s / --short` for concise output.

## Commit staged files

`git commit -m "{commit message}"`

## .gitignore

The rules for the patterns you can put in the .gitignore file are as follows:

- Blank lines or lines starting with # are ignored.
- Standard glob patterns work, and will be applied recursively throughout the entire working tree.
- You can start patterns with a forward slash (/) to avoid recursivity.
- You can end patterns with a forward slash (/) to specify a directory.
- You can negate a pattern by starting it with an exclamation point (!).

#### Examples
```
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
```

## Remote repos

### Push to

`git push origin master`

### Pull from
