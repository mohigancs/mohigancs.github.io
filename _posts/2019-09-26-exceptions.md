---
title: exceptions
---

### What is an exception? (abstract)

According to the [Java documentation](https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html), *an exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions*. Usually, exceptions refer to errors, since in Java all errors are actually classes that derive from the *Exception* class. 

### Example code

```java
public static void main(String[] args) {
	System.out.println("Hello World!");
}
```