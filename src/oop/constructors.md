# Constructors

A **constructor** is a method used to initialize objects. You can tell a method is a constructor because the name is always the same as the class name.

To create a constructor, we create it like a normal function without a return type.

A constructor with no parameters is known as a *no-args constructor*.
```java
public class Fruit {

    // A no-args Constructor:
    public Fruit() {

    }
}

void main() {
    // Fruit() calls the constructor.
    Fruit apple = new Fruit();
}
```

## Constructor with Parameters
A constructor with parameters is known as a *parameterized-constructor*.
```java
public class Fruit {
    String name = "";

    // Constructor with a parameter:
    public Fruit(String fruitName) {
        name = fruitName;
    }
}

void main() {
    // Fruit("apple") calls the constructor
    // with "apple" as the argument.
    Fruit apple = new Fruit("apple");
}
```

### Multiple Parameters
```java
public class Fruit {
    String name = "";
    String color = "";

    // Constructor with a parameter:
    public Fruit(String fruitName, String fruitColor) {
        name = fruitName;
        color = fruitColor;
    }
}

void main() {
    // Fruit("apple", "red") calls the constructor
    // with "apple" and "red" as the arguments.
    Fruit apple = new Fruit("apple", "red");
}
```

## Copy Constructor
A **copy constructor** is a variant of a normal constructor. It usually takes one parameter that is of the same type as the class.

This follows by setting each relevant member field equal to the object we're copying's member field.

```java
public class Fruit {
    public String name = "";
    public String color = "";

    // Parameterized Constructor
    public Fruit(String fruitName, String fruitColor) {
        name = fruitName;
        color = fruitColor;
    }

    // Copy Constructor
    //  where <other> is some other Fruit object.
    public Fruit(Fruit other) {
        name = other.name;
        color = other.color;
    }
}
```

We then pass some other object of the same class to our copy constructor.

```java
void main() {
    Fruit apple = new Fruit("apple", "red");
    Fruit anotherApple = new Fruit(apple);

    IO.println(anotherApple.name);
    IO.println(anotherApple.color);
}
```

```
Output:
apple
red
```