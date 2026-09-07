# The This Reference
`this` is another variant of a reference variable. It **refers to the current object**. It can only ever be used within instance methods, constructors, or initializer blocks.

## Variable Shadowing
**Variable Shadowing** occurs when a variable declared within an inner scope has the same name as a variable declared in the outer scope.

```java
public class Animal {
	// <outer scope>
	public String name = "";

	public Animal(String name) {
		// <inner scope>
		// The parameter <name> has the same identifier
		// as our member field.
	}
}
```

We can differentiate between the two by using `this`.
```java
public class Animal {
	// <outer scope>
	public String name = "";

	public Animal(String name) {
		// <inner scope>
		// name refers to the parameter.
		// this.name refers to the member field of the current object.
		this.name = name;
	}
}
```

It becomes good practice to use `this` whenever we are wanting to use some value that is a member field.