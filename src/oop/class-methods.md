# Class Methods
We know that [**methods**](../intro/methods.md) are a way to have resuable blocks of code to keep things clean. We can define a method within a class through the following syntax:

```
<visibility modifier> <return type> <method name>(<parameters>) {
	<code>
}
```

```java
public class Fruit {
    String name = "apple";

    // Fruit's class method: printName.
    public void printName() {
    	IO.println(name);
    }
}

void main() {
	Fruit apple = new Fruit();
	apple.printName(); // "apple"

    Fruit orange = new Fruit();
    orange.name = "orange";
    orange.printName(); // "orange"
}
```