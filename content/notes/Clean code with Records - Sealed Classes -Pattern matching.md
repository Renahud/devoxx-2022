---
title: "Clean code with Records - Sealed Classes -Pattern matching"
---
by *José Paumard*

new features of [[notes/java 19 |Java19]]

## [[notes/Record class|Record]]

```java
public record Point(int x, in y){}
```

A record is a child of the Record class, so it cannot extend anything.
It 's immutable.

Override the **cannonical constructor** for:
- It's a good idea to create a defensive copy of an arraylist that you pass to make it really immutable. 
- validation

**Compact constructor
- for validation


> [!WARNING] 
> You cannot create a constructor that doesn't call the cannonical constructor


## [[notes/Pattern Matching |Pattern Matching]]

Adding responsability to your business model is not always a good idea.
Violates the single responsability principle.

If you externalize that responsability, you will have to do some casting to process subclasses.

=> patternMatching for *instanceOf* 

First step into pattern matching.

can be used in [[notes/switch expressions|switch expressions]].
```java
return switch(shape){
	case Circle circle -> ...
	case Square square -> ...
	default -> ...
}
```
in this example : `Circle circle` is a pattern


### Sealed type

a type that knows it's extensions.
```java
public sealed interface Shape
permits Circle, Square{

}
```

If the class is sealed, you don't need the default value in the switch :

```java
return switch(shape){
	case Circle circle -> ...
	case Square square -> ...
}
```

Using this, you can make sure you have an implementation for all the sublasses of a type, it's safer.

Next step in pattern matching: **record pattern matching**

Next :
Array Patten Matching
Nested Patterns
Patterns from existing classes

#readMore 