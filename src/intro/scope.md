# Scope and Globals

## Scope
The area in which we define variables is referred to as the **scope**. In Java, scope is the area where we place "code blocks" in between curly braces (`{}`). 

Once a variable reaches the end of the scope it's in, the variable can no longer be used. The duration of a variable being considered valid for use vs invalid for use is called its **lifetime**. 

For example:
```java
void main() { // "main" scope start
	int x = 0;

	if (x == 0) { // "if" scope start
		int y = 100;
	} // "if" scope end, y no longer available.

	// Since the scope that y was created in has ended,
	// we can no longer use y unless we define it again.

} // "main" scope end
```

Since a variable cannot be used after the scope in which it was created in ends, we have to define it again:

```java,runnable,scope_0
void main() { // "main" scope start
	int x = 0;

	if (x == 0) { // "if" scope start
		int y = 100;
	} // "if" scope end, y no longer available.

	// IO.println(y); --> Error

	int y = 200;
	IO.println(y); // --> 200;


} // "main" scope end
```

```
Output:
200
```

## Global Variables
A global variable is a variable whose lifetime is attached to the whole program or "global scope".

This can be defined using the `static` keyword:

```java,runnable,scope_1
static int x = 10;

void main() {
	IO.println(x);
}
```

```
Output:
10
```

Globals can also be constant by using `final`.
```java,runnable,scope_2
static final double PI = 3.14;

void main() {
	IO.println(PI);
}
```

```
Output:
3.14
```

