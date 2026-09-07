# Finalizing our Example
Now we can revisit the example from the [encapsulation page](encapsulation.md). Our current code so far looks like:

```java
public class Person {
    public String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Setter for age:
    public void setAge(int age) {
        this.age = age;
    }

    // Getter for age:
    public int getAge() {
        return this.age;
    }
}
```

We can prevent our age member field from going below 0 by validating the user-supplied age before setting it.

```java
public class Person {
	...

	// Setter for age:
	public void setAge(int age) {
		// Ensure age cannot go below 0.
		if (age < 0) {
			age = 0;
		}
		this.age = age;
	}

	...
}
```

We can then use `setAge` in our constructor ass well.
```java
public class Person {
	...

	public Person(String name, int age) {
		this.name = name;
		setAge(age);
	}

	...
}
```

**The only way to modify the age member field is to use our setAge method**. Even when instantiating the object, we internally call `setAge` to have the argument go through our validation.

We have now protected the integrity of our `age` member field using encapsulation.
```java
void main() {
	Person personA = new Person("Charlie Brown", -100);
	IO.println(personA.getAge()); // 0

	personA.setAge(-200);
	IO.println(personA.getAge()); // 0

	personA.setAge(75);
	IO.println(personA.getAge()); // 75
}
```