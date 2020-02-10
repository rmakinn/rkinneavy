---
Title: "Go"
draft: true
bookCollapseSection: true
---

# Golang

https://golang.org/doc/faq

## Notes

- The pkg sources are excellent examples of how to use the language, idioms etc
- Seems like slices, structs, and idiomatic approaches to interfaces, methods, errors are core to writing things correctly and non-noob
    - Grokking the concurrency stuff may be hard https://golang.org/doc/effective_go.html#concurrency
- Read through this stuff without stressing all the details (except the syntax ofc), move on to...
- lack of utility functions leads to transparency thru understanding
- init cycles in pkgs lead to no compile: https://yourbasic.org/golang/package-init-function-main-execution-order/
- regex in go is fast
- the GC is good: https://blog.golang.org/ismmkeynote
    - write a summary article? 
- receiver = javan 'this'
- ooooohhhhh Go/Java === `Public` and `private`
- Go by Example is really fantastic: https://gobyexample.com/hello-world

---

# TODO?

## Go Tour exercises

- loops and functions sqrt 
- slice exercise: frustruating picture one
- word count maps
- fib closure
- etc etc

## Understanding

- Pointer gneration & deref'ing
- Slices and range
- Methods & value/pointer receivers
- interfaces; implicit, empty, practical usage; assertion/test/switches
- Error handling, reader.io, images
- Goroutines
- Channels
- sync.Mutex


## Pages/notebooks to create

- Gotchas
- Note for each basic/complex datatype
- External things: OS, filesystem, SQL, datetime
- Testing workflow, features
- Core features: concurrency, web back-end programming: https://yourbasic.org/golang/concurrent-programming/
- Paradigm support
- Cool things from stdlib
- Examples:
    - Common tasks
    - Algorithm implementations
    - 


---

### What to learn - programming

- control flow and patterns
- application design
- os/network/web protocols and concepts
- API design: https://yourbasic.org/algorithms/your-basic-api/

### What to learn - Go

- syntax
- naming conventions
- 


### Order

#### Day 0

https://github.com/golang/go/wiki#getting-started-with-go

- Tour of Go [3/5]
    - Methods/interfaces
    - Concurrency primitives
- How to Write Go Code: https://golang.org/doc/code.html
    - Project structure
    - PATH
    - Go cmds
    - Testing
- Language spec: https://golang.org/ref/spec
    - Types
    - Declarations & scope
    - Expressions
    - Statements
    - Built-in functions
    - Pkgs
    - Program init & exec
    - Errors & panics
- Standard library documentation: https://golang.org/pkg/

#### Day 1

- Effective Go: https://golang.org/doc/effective_go.html
- Official example Wiki: https://golang.org/doc/articles/wiki/

### Projects

- Web: using net/http
    - SSG
    - Wiki
    - Server: https://gobyexample.com/http-servers
    - App
    - Scraper
    - Misc network programming: https://jan.newmarch.name/go/
- CLI
    - Pocket/similar dl'er
    - https://yourbasic.org/golang/write-command-line-application/
    Shit like this:
    - https://github.com/ok-borg/borg
    - https://github.com/golang/go/wiki/Projects
    - https://github.com/SeungheonOh/GoHome
- Script for init'ing a Go project, like: https://github.com/yourbasic/fenwick
- Discord/Telegram bot
- Game server
- AStar implementation: https://github.com/beefsack/go-astar
- Cubing solver/stuff
- electron app https://github.com/asticode/go-astilectron
- ML/AI: bayesian/text classification, OCR, tensorflow, recommender system (gorse)
- Excel interaction
- Auto-tagging for pkb/site https://github.com/zoomio/tagify
- https://github.com/aerogo/aero
- gitea hacking
- interpreter/compiler in Go
- 


### Examples

https://yourbasic.org/golang/blueprint/



### Resources

https://golang.org/doc/
https://talks.golang.org/
https://go101.org/article/details.html
