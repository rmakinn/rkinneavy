---
Title: "Memory"
bookCollapseSection: true
draft: true
---

# Memory

Memory management is an important sub-topic of both application programming and operating systems. 

For the programmer, it's a primary and persistent concern when working in languages like C, Rust, and C++. For the system or application architect, it's critical to understand (although less frequently recalled) when working with dynamically-allocated, garbage-collected languages like Go and Python.

Understanding it has some nice benefits - it will evolve the way you write code, tending toward more performant programs with fewer bugs. For people like me who have an urge to grasp things all the way up and down, it's intrinsically rewarding.

I'll be straight with you - mis-understanding it is more costly than understanding it is beneficial. Bad allocations, untracked multiple references, segfaults, GC-induced stalls not observable in testing, etc etc. All sorts of malicious attacks and critical bugs are down to poorly-managed memory.



#### Links
- [WikiPedia](https://en.wikipedia.org/wiki/Memory_management)
  - [MM4OS](https://en.wikipedia.org/wiki/Memory_management_(operating_systems))
- [Memory Management Reference](https://www.memorymanagement.org/mmref/index.html) (Intro)
- [What Every Programmer Should Know About Memory](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf) [PDF]
  - Also posted in [article](https://lwn.net/Articles/250967/) format at LWN.net (1st of 9 parts)
- [Linux Memory Management](https://linux-mm.org/LinuxMMInternals)

#### Topics

- Static & Dynamic Allocation
- Virtual Memory
- Garbage Collection
- Segmentation
- Safety
  - Rust

---

## References


#### Safety

- Normal Accidents. Perrow, Charles
  - [Wikipedia](https://en.wikipedia.org/wiki/Normal_Accidents)
  - [In retrospect: Normal Accidents](https://www.nature.com/articles/477404a)
```
@article{Pidgeon2011,
  doi = {10.1038/477404a},
  url = {https://doi.org/10.1038/477404a},
  year = {2011},
  month = sep,
  publisher = {Springer Science and Business Media {LLC}},
  volume = {477},
  number = {7365},
  pages = {404--405},
  author = {Nick Pidgeon},
  title = {In retrospect: Normal Accidents},
  journal = {Nature}
}
```

- Safeware: System Safety and Computers. Leveson, Nancy G.
```bibtex
@book{10.1145/202709,
author = {Leveson, Nancy G.},
title = {Safeware: System Safety and Computers},
year = {1995},
isbn = {0201119722},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA}
}
```
