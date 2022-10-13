---
title: "The art of java language Pattern Matching"
alias: []
---

Historically, we've had *java.util.regex*.

That's not the subject, it's gonna be about [[notes/Pattern Matching|language level patterns]].

A pattern is
- a match predicate : determines whether the pattern matches a target
- pattern variables : conditionally extracted if the pattern matches the target.

## Pattern Types
- constant
	- match on a constant (already un use in a switch statement)
- Type
	- match on a type
- Deconstruction
	- Match and extract
- var
	- Uses type inference to map to a type pattern
- Any( _ )
	- Matches anything but binds to nothing (an unused pattern variable)


## Switch Expressions
Used to be a statement. No concept of generating a result that could be assigned
Error prone if you forget the `break;` statement.

=> [[notes/switch expressions | Switch Expression]]
Now the switch returns a value.
- The compa$iler can check that we always have a value
- tidier
- immutable

## [[notes/Record class|Record]]
```java
record Point(double x, double y);

record Anything<T>(T t);
```

* Implicitly final.
* Don't follow the bean pattern
	* x(), not getX()
* base class is java.lang.Record
	* cannot be sublassed

## Inheritance
A class can be sub-classed by any class. No control on who can sublass
=> new Sealed Classes
`permits X, Y` 

