### Handling exceptions
Two ways to handle exceptions:
	
Use *try*, *catch*, *finally*

	Throw an exception

Catching exceptions...(referred to above as “handling” the exception). This uses *try*, *catch*, and *finally*.

```java
public class MyClass{

	public void myMethod(double d){

		…some code in which you are not worried about an exception occurring…
		try //if error occurs, rest of code doesn’t execute...jumps to appropriate catch{

			…some code where you might expect an exception…

			String s = in.nextLine( ); //might produce an IOException
			int x = Integer.parseInt(s); //bad s might produce a  NumberFormatException
			…more code…

		}

		catch (IOException e){

			System.out.println(“Input/output error ” + e);

			// Continues execution after last catch below.
		}

		catch (NumberFormatException e){

			System.out.println(“Input was not a num ” + e);

			// Continues execution immediately after this catch.

		}

		…code execution continues here after try block is finished…or, if an exception occurs, execution continues here after catch block finishes…

	}

}
```
	Usage of the *finally* block(this block is optional):
	```java		

		try{

		
}
		
catch( … ){
			…
		}

		finally{
			
…This block of code is guaranteed to execute, regardless of whether there was an exception or not.
			This is typically used to release resources, such as closing a file or releasing a network connection.
			If an exception occurs in the try block and none of the catch statements are appropriate to handle the exception, control passes to this finally block and the code here executes…
			then the exception is actually thrown and passed up the calling chain where we can attempt to catch it. Even if a catch block throws an exception of its own, control is still passed to the finally block.

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







