# Parameters and Arguments
Data can be passed into methods as a **parameter**. Parameters are specified after the method name within the parenthesis and separated by a comma:

```java,runnable,args_0
void greet(String name) {
	IO.println("Hello, " + name + "!");
}

void main() {
	greet("General the Jaguar");
}
```

```
Output:
Hello, General the Jaguar!
```

An **argument** is the term used for the data specified in the call. In the example above, `name` is a parameter and `General the Jaguar` is the argument.