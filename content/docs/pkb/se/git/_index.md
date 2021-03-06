---
Title: "Git"
bookCollapseSection: true
---

# Git

I use `git` to version code projects, interact with the hosting option of this website, and track my dotfiles - I also use it with my notes, and things like CVs and important applications.

A decent chunk of developers use `git`, and are comfortable with the basic actions like (git) `add`, `commit`, `push`, `pull`, `checkout`. They'll also view stuff with `git status -s`, `git log` and `git blame` day-to-day too. I'm not comfortable with more general commands like `merge`, `rebase`, or `stash` - and I'm unfamiliar the cornucopia of other commands `git` makes available. 

I don't have an overstanding of the underlying concepts. Asking around, it seems I'm not alone! My aim here is to summarise the technical information I can find on StackOverflow etc in fairly plain, expository prose. The distribution of explanations seems to be pretty two-tiered - one for the common-garden git commands and concepts (about 10% of those available), and another for fine-grained explanations of the remaining 90%. I'm going to have to bridge the gap -- my memory doesn't like to store things I don't [overstand]({{< relref "../../language/cool-words.md#overstand" >}}) -- so I may as well record my learnings here.

{{< hint info >}}
Btw, the book [**Pro Git**](https://git-scm.com/book/en/v2) by Scott Chacon is my main reference and much here is copied over liberally. Other references:
- [IBM Developer Tutorial](https://developer.ibm.com/technologies/web-development/tutorials/d-learn-workings-git/)
- [Mine of Information - Git Foundations](http://moi.vonos.net/programming/git-foundations/)
- [The Git Parable](https://tom.preston-werner.com/2009/05/19/the-git-parable.html)
{{< /hint >}}

## Sections

- [How Git works]({{< relref "how-git-works.md" >}})
  - Basic, plain-ish description of the underlying bits and pieces with plenty of out-links
  - Refer to https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain

- [Git cheatsheet]({{< relref "../../cheatsheets/git.md" >}})
  - TODO: Cover all the most common operations
  - TODO: Describe the less common but occasionally very useful actions, link to reference materials for when I do need to do them

- Git notes
  - TODO:
    - adding & staging
      - undoing & unstaging
    - git log & blame
    - remote mgmt
    - branches
    - collaboration
    - GitHub
    - Git Hooks
    - Useful commands
    - Git in CLI/TUI/VSCode
