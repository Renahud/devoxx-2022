---
title: "Confessions of a rusty java developer"
---

## What is RUST
- C-like syntax
- strongly typed (with inference)
- statements
	- variable bindings
	- expressions

### Most things are expressions
- functions
- variable assignments
- implicit return when no ";"

**Rust has no**
- null pointer
- exceptions

### Rust has algebraic data types.
 Enum have states
Option type, like optional in java
- some
- none
Result type:
- ok
- Err 

### Pattern matching and destructuring
examples were given

## Differences with java
- no garbage collector
- everything is immutable by default
- everything is private by default

### Ressource allocation
Memory is allocated in scopes and freed at the end of the scope

### Ownership
Only one owner to a memory value.
So you can borrow a reference, as long as it's immutable.

### Explicit lifetimes

you can specify hte lifetimes of hte memory allocations and some relationships between lifetimes.
=> The compiler educates you and the code becomes simpler and faster.

### Leads to clearer API's
When your dataflow is clearly defind, you can know very precisely how you're supposed to use an api and how the data will be used.
