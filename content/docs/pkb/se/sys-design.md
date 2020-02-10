---
Title: "System Design"
draft: true
bookCollapseSection: true
---

# System Design

## CAP Theorem

## Atomic R(M)W

https://stackoverflow.com/questions/22610603/atomic-actions-what-is-meant-by-reads-and-writes

> Essentially, a Read cannot occur when a previous Write has not yet returned. Means that there is no difference between simultaneous and linear processing of a set of similar R/M/W operations on some data store/register.

## Caching

Can be a 'shock absorber' during periods of heavy loads. Types:

Client side: OS or browser, server side, or in a distinct cache 'layer'
CDNs
Web server
DB caching
Application caching (In-memory caches i.e. memcached, redis; optimising for business-effective use of RAM vs disc)
LRU
Updating strategies/cache pipelines:

Cache-aside
Write-through
Write-behind/write-back
Refresh-ahead
Considerations:

Consistency between caches and source of truth is complex (see cache invalidation)
Application/logic adaptions for services like Redis or Memcached

## Concurrency

TODO: Research 'Back Pressure'

## Resources

https://slikts.github.io/concurrency-glossary/

https://eli.thegreenplace.net/2017/concurrent-servers-part-1-introduction/
