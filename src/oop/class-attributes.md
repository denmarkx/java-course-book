# Member Fields
**Member Fields** are variables declared inside a class. 

## Alternative Terminology
You may also hear member fields referred to as: fields, attributes, or properties.

```java
public class Fruit {
    // name is a member field.
    String name = "apple";
}
```

## Mutating and Accessing Fields
To access a field, we create an object of the class and use a dot (`.`) followed by the field name.

```java
public class Fruit {
    // name is a member field.
    String name = "apple";
}

void main() {
    // Accessing:
    Fruit apple = new Fruit();
    IO.println(apple.name) // "apple"

    // Mutating:
    Fruit orange = new Fruit();
    orange.name = "orange";
    IO.println(orange.name) // "orange"
}
```