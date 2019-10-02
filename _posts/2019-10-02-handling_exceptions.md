---
title: Handling exceptions
---

### Two ways to handle exceptions:
	
Use *try*, *catch*, *finally*

Catching exceptions...(referred to above as $$ \boldsymbol {handling} $$ the exception). This uses *try*, *catch*, and *finally*.

```java
public class MyClass{
	
	public void myMethod(double d){

		try {

			//some code where you might expect an excpetion

			String s = in.nextLine();
			//might produce an IOException

			int x = Integer.parseInt(s);
			//might produce a NumberFormatException

		}

		catch (IOException e){

			System.out.println("Input/output error " + e);

		}

		catch (NumberFormatException e){

			System.out.println("Input was not a num " + e);
			//Continues execution immediately after this catch.

		}

 
	}
}
```

Usage of the *finally* block(this block is optional):

```java
try {

}

catch () {

}

finally {

	//this block will always execute, regardless of an exception

}
```


Throwing exceptions... 
What's the purpose of the *throws* specifier? 
The purpose is so the calling-method (the method that called the *readTheDisk* method) is signaled that an *IOException* may occur in *readTheDisk* and that the calling method is to handle the exception. 
Of course, in the calling-method you can make the choice of putting another *throws* specifier in its signature, or to actually handle the exception right there with *try*, *catch*, and *finally*. 
Thus, we see that the *throws* specifier is a way to defer the handling of an exception. We can keep postponing the actual handling of the exception right up the calling chain. 
Of course we can defer it all the way up to the *main* method and if no *try-catch* is there, then the program terminates. The *throws* specifier can provide for multiple exceptions as in the following example:


Unchecked exceptions can also make use of *throws* to defer handling of the exception...
Or you can handle them at any level in the calling chain with try, catch, and finally. 
Unchecked exceptions need not be handled at all. You can just let the program terminate (crash) immediately upon detection of such an error.







