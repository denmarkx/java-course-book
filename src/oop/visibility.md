# Visibility Modifiers
Visiblity modifiers (sometimes called access modifiers) are a way to control the accessibility of class methods, member fields, etc. For now, we are looking at `public` and `private`.

Going back to our Person class, let's alter the visibility modifier of `age` to `private`.

```java
public class Person {
	public String name;
	private int age;

	public Person(String name, int age) {
		this.name = name;

		// This still works because we are within the class:
		this.age = age;
	}
}
```

..now let's try to set the age member field directly:
```java
void main() {
	// Works, but still has the negative 100 issue (which we'll look at next)
	Person personA = new Person("Charlie Brown", -100);

	// ERROR!! the <age> member field is now private.
	personA.age = -200;
}
```

We have restricted the access to the `age` member field by setting its visibility to `private`. But now, we need a way to read and maybe set it!