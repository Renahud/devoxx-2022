---
title: "Clean code with Records - Sealed Classes -Pattern matching"
---
by *José Paumard*

new features of [[notes/java 19]]

## [[notes/Record class|Record]]

A record is a child of the Record class, so it cannot extend anything.
It 's immutable.

Override the **cannonical constructor** for:
- It's a good idea to create a defensive copy of an arraylist that you pass to make it really immutable. 
- validation

**Compact constructor
- for validation


> [!WARNING] 
> You cannot create a constructor that doesn't call the cannonical constructor



