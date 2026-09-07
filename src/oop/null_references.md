# Null References
Java has a special type of reference called a **null reference**. This means that the reference variable **does not refer to any piece of memory**.

Let's say we had a String in our member field that was not given a default value:

```java
public class Animal {
	public String species;
}
```

This is equivalent to writing:
```java
public class Animal {
	public String species = null;
}
```

..because we have not given a specific piece of memory for the `species` reference variable.

## NullPointerException
If we try to call a method on a null reference, we get a `NullPointerException`:

```java
void main() {
	Animal parrot = new Animal();
	parrot.species.toUpperCase();
}
```

```
Output:
java.lang.NullPointerException:
	Cannot invoke "String.toUpperCase()"
	because "<local1>.species" is null.
```

In the event that we want to check if a reference is null, we can use an if statement:

```java
void main() {
	Animal parrot = new Animal();
	if (parrot.species != null) {
		IO.println(parrot.species.toUpperCase());
	}
}