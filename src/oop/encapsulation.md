# Encapsulation
**Encapsulation** is the process of restricting access and mutation to an object's internal representation.

## When Encapsulation is Useful
* **Data Integrity**: By exposing certain methods, we can control the way outside code can use our member fields.
	* **Validation**: We can validate incoming data before it changes internal state.
	* **Mutability**: Creating a read-only field.
* **Maintenance**: Internal code can be changed without breaking other classes that use it.

### Example
Let's consider an example of when encapsulation would be useful by looking at a class for a Person:

```java
public class Person {
	public String name;
	public int age;

	public Person(String name, int age) {
		this.name = name;
		this.age = age;
	}
}
```

The `age` member field is currently public. Thus, anyone can create some code like this:
```java
void main() {
	Person personA = new Person("Charlie Brown", -100);
}
```

This is not good! The age member field should never go below 0.

..keeping that in mind, let's revisit this example after introducing ways to apply encapsulation in our code.