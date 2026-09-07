# Static Variables, Constants, Methods
We know that member fields are states attached to the object. Now, let's look at something that can be attached to the class and shared between *all* objects.

For example, let's remember our BankAccount class. We want to track the total number of bank accounts created. If we were to make it a normal member field, the counter would be attached to each object. We can instead make it *static* so that it maintains its value across all objects.

To do this, we use our `static` keyword after our visibility modifier and before our data type.

```java
public class BankAccount {
	// ...
	private static int totalAccounts = 0;
	// ...
}
```

We can update our counter in our constructor.

```java
public class BankAccount {
	// ...

	BankAccount() {
		totalAccounts++;
	}
}
```

Since our `totalAccounts` member field is static, we need to have a static method to access it.
```java
public static int getTotalAccounts() {
	return totalAccounts;
}
```

Class methods that do not use static are referred to as **instance methods**.

Since our getter method is static, it is not attached to any object. It is attached to the class. To call it, we specify the class first: `BankAccount.getTotalAccounts()`.

Let's look at this in action:
```java
void main() {
	BankAccount accountA = new BankAccount();
	IO.println(BankAccount.getTotalAccounts()); // 1

	BankAccount accountB = new BankAccount();
	IO.println(BankAccount.getTotalAccounts()); // 2
}
```

## Summary
Let's look at when to use static vs instance methods.

| Scenario | Static Method | Instance Method |
| -------- | ------------- | --------------- |
| State | Shared across all objects. | Unique to each object |
| Behavior | Independent of object state (ie: utilities) | Dependent on individual object's data |
| Memory | Allocated once when class loads | Allocated every time a new object is created |