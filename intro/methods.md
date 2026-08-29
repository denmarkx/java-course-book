# Methods
In Java, the term "function" and "method" is (mostly) interchangeable.

A method is some reusable block of code that is only run when it is called. Optionally, the method can return some data.

The general syntax for methods in Java is:
```
<return type> <method name>() {
	...
}
```

If a method does not return any data, the return type is **void**.

Example:
```java,runnable,methods_0
void greet() { // Define the greet method.
	IO.println("Hi there!");
}

void main() {
	greet(); // Call the greet method.
}
```

```
Output:
Hi there!
```

```java,runnable,methods_1
String greet() { // Define the greet method.
	return "Hi there!!";
}

void main() {
	// Call the greet method.
	// Assign its return value to the "greeting" variable.
	String greeting = greet();

	IO.println(greeting);
}
```

```
Output:
Hi there!!
```
