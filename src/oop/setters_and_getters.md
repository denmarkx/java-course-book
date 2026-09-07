# Setters and Getters
Setters and getters are special methods used in applying encapsulation to control the way outside code writes and reads to our member fields.

**Setters**: A method that writes to some member field is caled a **setter**. By convention, programmers prefix these functions with `set`.

**Getters**: A method that reads a member field and returns some representation of that member field (or the field directly) is called a **getter**. By convention, programmers prefix these functions with `get`.

## Application
Applying setters and getters to our `Person` class:

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
