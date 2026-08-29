# Syntax and Entry Point

The **entry point** of a program is defined by the `main` function.

No need to worry about the keywords such as `void` right now. What is most notable with respect to the syntax is the use of parenthesis, curly braces, and semicolons.

Notice in the example below that each parenthesis and curly brace has a matching end.

```java
void main() {
}
```

## Comments
There are a few ways to write comments in Java. Comments do not run and are meant as explanatory text for the code.

**Single-line Comments**:

Use two forward slashes: `//`

```java,runnable,syntax_1
void main() {
	// Print out "Hi!" to console.
	IO.println("Hi!");
}
```

```
Output:
Hi!
```

**Multi-line Comments**:

Multi-line comments begin with a `/*` and end with a `*/`. Any text in between will be treated as a comment.
```java
/*
 Multiline
 Comment!
*/
void main() {
	...
}
```