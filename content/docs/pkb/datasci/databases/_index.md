---
bookFlatSection: false
bookCollapseSection: true
title: "Databases"
---

# Databases

{{< hint info >}}
I think learning about databases and implementing a simple one makes an excellent challenge and proof-of-skill for me as a self-taught programmer.

It goes without saying they're ubiquitous in industry. Taking a look at the concepts, they're also very interdisplinary, requiring: 

- algorithms & data structures
- networks
- operating systems
- hardware 

Hence they tend to appear in CS degrees in the 2nd year onward.

In contrast, *not* knowing much about how they work can be a hindrance when it comes to tasks like writing complex yet performant queries, designing schemas, or managing weird edge cases when using ORMs.

{{< /hint >}}

This section will be a central location of resources and notes on databases while implementing a toy DB myself.

## Big List of Resources

A bit of redundancy here but they're all of high quality, mostly sourced from various lists/posts online. 

[Tags] indicate resource type

[*] = priority

### SQL

- [Khan Academy](https://www.khanacademy.org/computing/computer-programming/sql) [Tutorial] [*]

- [SelectStarSQL](https://selectstarsql.com/) [Tutorial]

- [Wikibook - SQL](https://en.wikibooks.org/wiki/Structured_Query_Language) [Textbook]

  - [Exercises](https://github.com/XD-DENG/SQL-exercise) [Repo] [*]

- [Tuning SQL](https://blog.tuningsql.com/) [Blog] [Advanced]

- [Use The Index, Luke!](https://use-the-index-luke.com/) [Book]
  - [SQL Performance Explained](https://sql-performance-explained.com/) [Book] [$$$]

### General

- [Let's Build a Simple Database](https://cstack.github.io/db_tutorial/) [DIY] [*]

- [db-readings](https://github.com/rxin/db-readings) [Repo] [List]

- [Readings in Database Systems](http://www.redbook.io/) [Textbook]

- [CMU 15-445/645 - Database Systems](https://15445.courses.cs.cmu.edu/fall2019/) [Course]

- [CMU Database Group](https://www.youtube.com/channel/UCHnBsf2rH-K7pn09rb3qvkA) [Channel] [*]

  - [CMU - Intro to Database Systems](https://www.youtube.com/playlist?list=PLSE8ODhjZXjbohkNBWQs_otTrBTrjyohi) [Course] [Playlist]

  - [CMU - Advanced Database Systems](https://www.youtube.com/playlist?list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O) [Course] [Playlist] [Advanced]
  
  - [CMU - Databaseology Lectures](https://www.youtube.com/playlist?list=PLSE8ODhjZXjakeQR57ZdN5slUu2oPUr1Y) [Playlist]

  - [CMU - 7 Databases in 7 Weeks](https://www.youtube.com/playlist?list=PLSE8ODhjZXjY2xvwxuKjZT5qFH0sQga8_) [Playlist]

- [Prof. Dr. Jens Dittrich](https://www.youtube.com/channel/UCC9zrtAkl6yY4dpcnWrCHjA) [Channel]

  - [Databases: Motivation & Introduction](https://www.youtube.com/playlist?list=PLC4UZxBVGKtf-Yx_tyZGshHaJczA8jWAD) [Playlist]

  - [Query Planning and Optimisation](https://www.youtube.com/playlist?list=PLC4UZxBVGKtcZgLCrIUenuano53pbPpf1) [Playlist] [Advanced]
  
  - [Data Managing Design Patterns](https://www.youtube.com/playlist?list=PLC4UZxBVGKtfJTE5UQITsnsIPQVgJRN_i) [Playlist]

- [Stanford - Intro to Databases](https://lagunita.stanford.edu/courses/DB/2014/SelfPaced/about) [Course]

- [Database Internals](https://www.databass.dev/) [Book] [$$$]

- [7 Databases in 7 Weeks](https://7dbs.io/) [Book] [$$$]

- [Designing Data-Intensive Applications](http://dataintensive.net/) [Book] [$$$]

### Concepts

- [ACID](https://en.wikipedia.org/wiki/ACID)
  - [BASE](https://stackoverflow.com/questions/3342497/explanation-of-base-terminology)

- [Consensus](https://en.wikipedia.org/wiki/Consensus_(computer_science))

- [CAP Theorem]({{< relref "CAP.md" >}}) [Internal]

  - [PACELC Theorem](https://en.wikipedia.org/wiki/PACELC_theorem)
  
- [Conflict-free replicated data type](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type)
  
- [Chord (peer-to-peer)](https://en.wikipedia.org/wiki/Chord_(peer-to-peer))



### Distributed Databases

- [An Introduction to Distributed Systems](https://github.com/aphyr/distsys-class) [Course]

- [Bigtable: A Distributed Storage System for Structured Data](https://static.googleusercontent.com/media/research.google.com/en//archive/bigtable-osdi06.pdf) [Paper]

- [Dynamo: Amazon's Highly Available Key-value Store](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf) [Paper]

### NoSQL

- [Intro to NoSQL - Martin Fowler](https://www.youtube.com/watch?v=qI_g07C_Q5I) [Talk]

- [Use cases for NoSQL](https://stackoverflow.com/questions/2875432/use-cases-for-nosql) [StackOverflow]

- [Write a NoSQL Database in Python](https://jeffknupp.com/blog/2014/09/01/what-is-a-nosql-database-learn-by-writing-one-in-python/) [DIY]

- [AOSA - The NoSQL Ecosystem](http://www.aosabook.org/en/nosql.html) [DIY] 

- [Google Firebase - Structure Your Database](https://firebase.google.com/docs/database/web/structure-data) [Tutorial]

### ORMs/Libraries

- [Python - SQLAlchemy](https://github.com/dahlia/awesome-sqlalchemy#readme) [List] [Repo]

- [Go - database/sql](http://go-database-sql.org/?ref=cybrhome) [Tutorial]

### Graph DBs

- [AOSA - Dagoba: an in-memory graph database](http://aosabook.org/en/500L/dagoba-an-in-memory-graph-database.html) [Tutorial]

### Other Misc


- [Hyperpolyglot - comparing SQL, Awk, Pig](http://hyperpolyglot.org/data)
- [Oracle - SQL for Web Nerds](http://philip.greenspun.com/sql/)
- [SQLite](https://www.sqlite.org/index.html) [*]
  - [SQLite Browser Online](https://extendsclass.com/sqlite-browser.html)
- [Redis](https://redis.io/)
- [Datomic](https://www.datomic.com/)
- [Neo4j](https://neo4j.com/)
  - [How the ICIJ Used Neo4j to Unravel the Panama Papers - Mar Cabra](https://www.youtube.com/watch?v=S20XMQyvANY)
  - [Graph Database Use Cases](https://neo4j.com/use-cases/)
- [CockroachDB](https://www.cockroachlabs.com/)
- [Riak](https://docs.riak.com/)
- [Mongo](https://www.mongodb.com/)
- [Memcached](https://memcached.org/)
- [Apache CouchDB](https://docs.couchdb.org/en/stable/) [Docs]

- [NoSQL Data Architecture & Data Governance: Everything You Need to Know](https://www.dataversity.net/nosql-data-architecture-data-governance-everything-need-know/) [Article]

- [NoSQL vs SQL: Demystifying NoSQL Databases](https://build5nines.com/nosql-vs-sql-demystifying-nosql-databases/) [Article]
