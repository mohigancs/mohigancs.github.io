---
title: exceptions
---

### What is an exception? (abstract)

According to the [Java documentation](https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html), *an exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions*. Basically, an exception is a special condition that is unexpected during execution. Usually this is an error. In Java, all errors are classes that extend the builtin *Exception* class.

### Catching Exceptions

In most programming languages - Java included - there are *try* and *catch* keywords that allow the programmer to redirect execution flow if an exception is encountered. Take the below code for example, where an arithmatic error is thrown, because we tried to divide by zero. 

```java
public static void main(String[] args) {
	try {
		int a = 1 / 0;
	} catch (ArithmeticException exception) {
		System.out.println("Oh no!");
		System.out.println(exception);
	}
}
```

Keep in mind, if we comment out the line containing the `1 / 0`, the `catch` block will never run since there was never an error thrown.

<!-- Add in more examples and use finally statements -->

### Why Exceptions are Important

If you are running an application for a large company and an error occurs, you probably want the user to see 

```
Internal Server Error: Please Contact Support
```

rather than something like the following...

```
java.sql.SQLException: Transaction (Process ID 57) was deadlocked on lock resources with another process and has been chosen as the deadlock victim. Rerun the transaction.
  at net.SQLDiagnostic.addDiagnostic(SQLDiagnostic.java:368)
  at net.TdsCore.tdsErrorToken(TdsCore.java:2816)
  at net.jdbc.TdsCore.nextToken(TdsCore.java:2254)
  at net.TdsCore.isDataInResultSet(TdsCore.java:795)
  at net.sourceforge.<init>(JtdsResultSet.java:146)
  at net.sourceforge.executeSQLQuery(JtdsStatement.java:483)
  at net.jtds.executeQuery(JtdsPreparedStatement.java:777)
```

Verbose errors like the one above are not only ugly and confusing for a customer but could also give a hacker compromising information about the server that the code is running on. 

### Making Custom Exceptions

Coming Soon!