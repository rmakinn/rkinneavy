# *There's no place like $HOME~*

Below I describe my home folder layout and why I do things the way I do, perhaps you'll get something out of it. It's a little excessive, I know, but what can you do? 🤷‍♂

---

```
.
├── archive        # old files by creation year, maybe useful again
    ├── 2019       
        └── 2019-01-01_file.txt # ISO-8601 date format is king, fight me
    └── 2020        
|
├── backups        # I use restic (and timeshift, but not in this dir)
|
├── inbox          # where all my unsorted downloads begin
|
├── library        # actually a symlink to my Dropbox folder on a secondary HDD
    |              # ^^ sorted downloads end up here
    ├── art
    ├── books
        ├── {DDS/LoC}  # classification schema
        └── shelf      # currently reading or soon-to-read
    ├── music
    ├── photos
    ├── scrots     # aka screenshots
    ├── videos
    └── walls      # aka wallpapers
|
├── org            # life admin: CVs, bank statements etc 
|
├── projects       # code, websites etc
|
└── wiki           # a bunch of interlinked markdown files, once managed by vimwiki
    └── diary      # I've since moved to Joplin as it's became really awesome in 2019.
```

## General notes

Liberal use of symlinking and the use of templates are the important bits here. It took a minute to understand how to use symlinks properly, but now they're something of a hammer, and I find nails everywhere. 

I took a bit of inspiration from systems like GTD and PARA - not that I'd ever advise getting too into these beyond reading a brief tl;dr, as I find them a heinous procrastination trap. Actually getting to this point involved a bunch of trial & error, setting things up and tearing them down repeatedly (and frankly, involved a big change in character - I use to be far less well-organised in every aspect).

### XDG

If you want a custom configuration like this and find that some applications make their own folders according to the default XDG spec (~/Desktop, /Documents etc - Firefox is particularly criminal of this), create a [user-dirs.dirs](https://wiki.archlinux.org/index.php/XDG_user_directories) file in your `~/.config` directory and edit it accordingly.

## By directory

### `archive/`

Old or stale stuff goes here. Could be code projects, old documents from Uni or previous workplaces, abandoned tutorials, whatever. I'm loathe to delete things, and this is how I manage it!

### `backups/`

This directory is also symlinked over to my 2nd HDD.

I use [restic](https://restic.net/), which genuinely does do backup right. Highly recommended, easy to schedule with a tool like `cron` or [`snooze`](https://github.com/leahneukirchen/snooze) .

I target folders like `~/projects` - it’s not in my Dropbox because, IIRC, Dropbox can run into trouble with symlinks in a certain direction, and with `git`. I use GitHub for all my projects anyway.

### `inbox/`

Self-explanatory - browser, website archiving or media downloads, Github checkouts etc.

I set up a script (TODO: link) to give me notifications to clean it up on Monday and Friday evenings.

Currently Firefox can only save to a single folder, or gets the user to select one every time. Someday I'll write a script I can get Firefox to call that matches download filetypes to specific locations.

### `library/`

As I mentioned this is just a symlink to a directory with that name on a secondary HDD mounted at `/media/data/Dropbox` - I have the same-sized SSD and HDD in both my computer and my laptop, and an identical setup, so I don't have to think much about selective downloads with Dropbox or messing much with configs. One day I'll upgrade to 2TB drives to match my Dropbox capacity.

#### `./books/`

I'm a data hoarder, and have many, many gigabytes of PDFs, ebooks and documents (surely more than a lifetimes worth already). I use something like the Dewey Decimal System to organise my books sub-directory - it works pretty nicely most of the time, although it's by no means perfect. 

For my general reading shelf, I put symlinks to the actual file in the library, and I do the same when I have books or PDFs related to projects. Saves a lotta space.

### `org/`

Not much to say. Usually this folder stores documents related to life-admin that I can't simply write and store in Joplin.

When I was playing around with `org-mode` I stored my `.org` files here. I want to come back to emacs at some point, but it's a huge time investment with long-term payoffs, and those kinds of costs are best paid for when I have a techie-job to fix my learning priorities, and to give me more schedule and certainty.


### `projects/`

My projects directory is full of projects fitting a template format, where I group code downloaded from related github repos and various documents and screenshots etc symlinked in from my library. 

I'll go into the directory structure another time.


### `wiki/`

Stuffed full of markdown files, but effectively archived - I'm in the process of clean-up and extraction as I type this very sentence.
