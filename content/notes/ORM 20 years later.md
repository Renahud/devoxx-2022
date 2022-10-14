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
- missing features of modern sql in HQL

Hand written code can still be as discomfortable... so it's not fair to only blame hibernate.

Hibernate did not properly communicate the option of using a **StatelessSession**

## Hibernate 6
Every once in a while it's time to break things...

They've rethought most API's and even removed some.
They support jakarta persistence and JPA3.

Brand new implementation of HQL/JPQL.

Stricter type ckecking, better error reporting.

Hql has a lot of functions that can be used on all databases.

Better support for dates and times, including time arithmetics.

Support for report-style queries.

Higher quality DDL generation.

Reworked type system for custom type mappings using annotations.

## Hibernate Reactive
(still based on H5 right now)

