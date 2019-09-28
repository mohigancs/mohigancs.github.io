---
title: big O notation
---

### what is big O?

*Big O Notation* is used in Computer Science to describe the performance or complexity of an algorithm. Big O can be used to describe the execution time required or the space used by an algorithm.

### constant time: $$ \boldsymbol{O(1)} $$

*Constant time* is when operations take a fixed, or constant time. This may be when you assign a value to some variable, insert an element into an array, determine if a binary number is even or odd, etc. 

```java
public static void main(String[] args) {
	int num = 5;
	int array[] = [1, 2, 3, 4, 5, 6, 7, 8, 9];
	System.out.println(array[num]);
}
```
All of these operations take a constant time because they are basic statements that only need to happen one time. In this case we say the statement time is $$ O(1) $$.

### linear time: $$ O(n) $$

*Linear time* indicates that an operation will execute $$ n $$ times. Linear time is said to have a complexity of $$ O(n) $$.

```java
public static void main(String[] args) {
	for (int i = 0; i < n; i++){
		// operation that will repeat n times
	}
}
```

Some examples of linear time are finding an item in an unsorted collection, or sorting an array with bubble sort.

### quadratic time: $$ O(n^2) $$

In this example the first loop executes $$ n $$ times. For each time the outer loop executes, the inner loop executes $$ n $$ times. Therefore, the statement in the nested loop executes a total of $$ n * n $$ or $$ n^2 ** times. The complexity is $$ O(n^2) $$. Quadratic time algorithms should be avoided as the computational complexity will grow very quickly (at a quadratic rate). 

```java 
public static void main(String[] args) {
        for (int i = 0; i < n; i++){
                for (int j = 0; j < n; j++){
			// operation that will repeat n^2 times
		} 
        }
}
```
Some examples of quadratic time are performing a linear search in a matrix, insertion sort, etc.

### logarithmic time: $$ O(\log(n)) $$

coming soon! 
:thonk:
