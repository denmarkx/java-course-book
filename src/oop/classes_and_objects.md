# Classes and Objects
A **class** is a blueprint that defines rules, variables, and actions for some *thing*. An **object** is a real representation of that *thing* created from that blueprint.

Example: "Fruit" would be a class. An apple, orange, or strawberry would be an object.

Another example: "Person" would be a class. Charlie Brown, Lucy van Pelt, would be objects.

## Creating a Class
To create a class, we'll use the `class` keyword followed by the class name. In Java, all classes begin with a capital letter.

`public` in this case is a [**visibility modifier**](visibility.md).

```java
public class Fruit {

}
```

## Creating an Object
To create an object in Java, we use the `new` keyword.

"Creating an object" is what we call **object instantiation**. We are creating an **instance** of the class.

```java
void main() {
	// Instantiate two new objects.
	Fruit apple = new Fruit();
	Fruit orange = new Fruit();
}
```
