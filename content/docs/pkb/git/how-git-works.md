---
Title: "How Git Works"
bookCollapseSection: true
---

# So how does git work? 

{{< hint info >}}
As I mentioned in the index of this section [**Pro Git**](https://git-scm.com/book/en/v2) by Scott Chacon is my main reference and much here is copied over.
{{< /hint >}}

## Sequential snapshots

Each occasion you give a (folder of) file(s) to git, it uses a **sequence of snapshots** to make a new version. These versions are stored in a repository (aka repo). 

Instead of the classic versioning system we're all familiar with from our school days, '`presentation final final.ppt`' and '`presentation final final final minus intro.ppt`', git avoids multiple redundant copies of files across versions. It's internal model reduces replication, and stores what's unique about each version from the get-go.

When building a new version:
- If a file *hasn't* changed between versions, the snapshot from the previous version is re-used. 
- If a file *has* changed between versions, git stores the new contents instead.

This logic works all the way down with git. That means you can have an identical file in your first snapshot as in the hundredth [0] - and another that might change on every version. 

Git also doesn't store multiple copies of a file. It tries to reduce replication *within* versions too. If you have hundreds of identical copies of a file in a repository, and say you name them all something different, git will still only store one copy and all those other filenames will point to it. "Huh, how?", I hear you ask.

### Hash

git runs some maths (called a *checksum*) using the **content** of a file, and produces a sequence of letters and numbers called a *hash* - the **name** of the file isn't given to the checksum. After it's finished working out the hash for the file, it associates the hash to the filename. If other files (titled whatever else you want) produce the same resulting number, git just adds more filenames alongside the original filename. Stupid example:

```
Let's say our checksum is really crappy and just reads some file 
in, & does whatever arithmetic it finds in the file. The results 
of the arithmetic are the 'hash' of this checksum. 

./Harry.txt
2+2 
    hash = 4

./Ron.txt
2+2
    hash = 4
    
./Hermione.txt
1+3
    hash = 4
```

| hash | name(s) |
|---|---|
| 4 | Harry.txt |
|   | Ron.txt |
|   | Hermione.txt |

The particular checksum used in git is the [SHA-1 Hash](https://en.wikipedia.org/wiki/SHA-1) algorithm. You give the algorithm some text (code, prose, numbers, whatever), and it spits out a sequence of letters and numbers of a predictable length. This algorithm is part of a group of algorithms called '[Cryptographic Hash Functions](https://en.wikipedia.org/wiki/Cryptographic_hash_function)', which are designed to be one-way [1] functions from some input to some output. 

This particular algorithm isn't perfect - it doesn't guarantee that an input will map uniquely to an output. In other words, even if you don't mean to, it's possible to get an output that is the same for two *different* inputs, aka a **collision**. In our toy example above, we can see that `Hermione.txt` contains 1+3, which gives a result that collides with the resulting hash of `Harry.txt` and `Ron.txt`.

You could mistakenly trust a safe file for one loaded with malware. As with all InfoSec stuff of this ilk - the more you trust it, the worse it is when it breaks [2]. More on the details [here](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html) and [here](https://shattered.io/).

Despite these little flaws, referring to files in a way that addresses their **content** rather than by **name** is very powerful - we'll get into why soon.

To summarise:
- Git is a version-control system which uses a checksum to track and compare the content of files.
  - The checksum isn't perfect but it's fine.
- It stores all of the initial commit, and afterward only the differences between each commit.

## Exploring a fresh .git/ repo

```
.
├── config                      # Project-specific options.
├── description                 # Ignore this (GitWeb).
├── HEAD                        # Points currently checked-out branch.
├── hooks                       # Fire off custom scripts when certain 
│  ├── applypatch-msg.sample    #   important actions occur.
│  ├── commit-msg.sample
│  [... etc ...]  
│  └── update.sample
├── info                        # Global exclude file for ignored patterns 
│  └── exclude                  #   you don’t want to track in a .gitignore.
├── objects                     # Stores all the content for your database.
│  ├── info
│  └── pack
└── refs                        # Stores pointers into commit objects in that 
   ├── heads                    #   above content/data, i.e. branches, tags, 
   └── tags                     #   remotes etc.
(yet to be created)
└── index                       # Where Git stores staging area information.
```

TODO: take notes from [Pro Git chapter 10.2](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects) onward.


---

[0] I wonder if open-source licenses from `npm init` templates are the most stable/re-used files across all the versions of all the git repos in the world.

[1] One-way = extremely difficult to 'invert' - to recover the input given just the output. 

[2] Although manufacturing a collision is super-expensive in terms of computer hours, and it's not like the hashing algorithm is being used by git to protect your bank details [2.1], git is planning to move to a better hashing algorithm called [SHA-256](https://en.wikipedia.org/wiki/SHA-2), although apparently it's [not proving too easy](https://www.theregister.co.uk/2020/02/05/git_sha_256_work/).

[2.1] Well, I hope not.
