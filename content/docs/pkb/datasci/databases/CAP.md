---
Title: "CAP Theorem"
---

# CAP Theorem

{{< hint danger >}}
Stub
{{< /hint >}}

## Links

[Wikipedia](https://en.wikipedia.org/wiki/CAP_theorem)

[FAQ](https://github.com/henryr/cap-faq)

[CAP Theorem Revisited](http://robertgreiner.com/2014/08/cap-theorem-revisited/)

---

## Patterns
### Consistency

- Weak (memchached, VoIP/chat, MRTS)
- Eventual (DNS, email)
- Strong (file systems, RDBMS)

### Availability

- Fail-over
- "heartbeat" connection between active/passive, hot/cold takeovers. Prev known as master/slave
- Load-spreading active/active, DNS/app logic must be aware of both
- Replication
