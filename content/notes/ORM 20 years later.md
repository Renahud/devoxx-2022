---
title: "ORM 20 years later"
alias: []
---

Avoid lazy fetching at runtime, but always map associations lazy.
use join fetch to eagerly fetch in specific queries.

Over time, the number of queries in an application grows much faster than the number of tables.

Sources of discomfort in hibernate :
- an extra library to learn and understand
- more difficult to debug and understand than some handwritten code
- error reporting was not the most helpfull in hibernate
- some users struggle dealing with managed entities and persistence contexts

Hand written code can still be as discomfortable... so it's not fair to only blame hibernate.

