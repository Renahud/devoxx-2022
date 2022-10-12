---
title: "Spring framework 6"
---

target  date : 2022-11

[[Spring Boot]] 3.0 : idem

Steps to spring boot 3
- Upgrate minor versions (migration guides)
- Java17
- Check depreciation in code
- Blog post on spring.io

Supporting Jakarta EE9+ 

### Exception handling
Using ExceptionsHandlers for each exception types returning more usefull infor to the clients.
Can be declared globally in a ControllerAdvice class

### AOT & [[GraalVM]]

### JAva interface client

Creating a simple rest client using a simple interface with 
```java
@GetExchange()
```

### [[notes/Project Loom|Loom]] Support