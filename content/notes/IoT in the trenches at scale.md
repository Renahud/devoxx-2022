---
title: "IoT in the trenches at scale"
alias: []
---
[[notes/Internet of Things|Iot]] usually follows a pattern

Sensors and actuators communicate with an application

but then there's a lot of questions that arise when you want to scale: 
- Bad communication
- monitoring
- remote management
- security
- ...

Fallacies of distributed computing:
- network is reliable
- latency is 0
- bandiwth is infinite
- network is secure
- topology doesn't change
- there's 1 administrator
- transport cost is 0
- network is homogeneous

The goal of the AWS components for [[notes/Internet of Things|IoT]] is to make this list seem true-ish.

Networks is always imperfact, communication will fail, you have to account for that all the time.

### Error handling

```java
try{
	leapOfFaith();
}catch(Throwable t){
	xyz();
}
```
This is not an anti-pattern in the world of IoT, it's the strength of Java to be able to recover from any kind of unpmanned error.

The modern JVM is available on a wide variety of wierd systems, so it makes java really good for IoT programming.
