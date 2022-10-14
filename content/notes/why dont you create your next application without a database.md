---
title: "Why don t you create your next application without a database"
alias: []
---

Database in this talk can be understood as any external storage out of your java application.

Data is everywhere and the vast majority of applications care about data and try to store them in some way.

The usual solutions to store data are databases, but there's a lot of complexity that comes with using them :
- Need for DBA
- Frameworks - hybernate
- caching
- mapping to objects
- Testability issues
- Statistics
- Slow Queries

How about we try something new ?

## JVM memory as Primary Data Source
JVM as database = Microstream
- Queries become easy with the stream API
- fast
- No convension
- Faster to develop

### Binary serialisation : Next generation java serialisation engine (MicroStream).

Stores a binary representation of the java objects :
- on disk
- in a no-sql database

Microstream will load your data in memory at runtime

## Demo

Just add the microstream dependency.

In your startup, you start a storagemanager.
The Data storage is just a pojo.


> [!NOTE] 
> Synergizes well with the new Record types

Storage configuration is configurable programmatically.

What about large collections of data that don't fit in hte HEAP ?

Possible of course, you can defin some lazy collections that will be loaded only when needed. Those lazy fields will be collected by the GC when he needs space, so they won't stay in memory.

