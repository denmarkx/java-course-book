# Variables
A **variable** is a "container" that can store a **value**. To declare a variable, you must first preface its name with the **type**.

The general syntax for variable declaration is: 

`<type> <identifier> = <value>;`

For example, below we are declaring an integer variable with identifier `x` and setting its value to `100`.

```java
void main() {
	int x = 100;
}
```

## Reassignment
The idiomatic term for "setting the value of a variable" is called **assignment**. Variables are what we call **mutable**, meaning its value can be reassigned after declaration:

```java
void main() {
	int x = 100;
	x = 5; // Reassignment.
}
```

## Constants
A constant is similar to a variable, except that is **cannot be reassigned**.

To declare a constant in Java, we use the `final` keyword to make the variable unchangeable:

```java
void main() {
	final int x = 100;
	x = 5; // Error!
}
```