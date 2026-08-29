# Strings

Strings are used to store text larger than a single character. They are surrounded by double quotes (`""`).

```java
void main() {
	String name = "General the Jaguar.";
}
```

## Concatenation
**Concatenation** is a fancy way of saying "combine". To *concat* two strings, we use the `+` operator.

```java,runnable,strings_0
void main() {
	String first_name = "General";
	String the = "the";
	String last_name = "Jaguar";

	IO.println(first_name + " " + the + " " + last_name);

	// ..or:
	IO.println("General" + " the " + "Jaguar");
}
```

```
Output:
General the Jaguar
General the Jaguar
```

## Numbers
Consider `int x = 10`, an integer. If we wanted to convert this to a string, we can use `Integer.toString`.

Recall, `int` is a primitive type while `String` is not. Therefore, type casting will *not* work here.

```java,runnable,strings_1
void main() {
	int x = 10;
	String num = Integer.toString(x);
	IO.println("The number is " + num);
}
```

```
Output:
The number is 10
```

# Quotation Marks
When writing a String, we use quotation marks: `String x = "Hi!"`. If we want to place a quotation mark inside the string, we need to **escape** it using a backslash (`\`):

```java
void main() {
	String x = "This is some sort of \"quote\".";
	IO.println(x);
}
```

```
Output:
This is some sort of "quote".
```

## Common Methods
There are several methods for Strings (see more here: [Java Docs - String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)).

### Length
`length` returns the length of the string.
```java,runnable,strings_2
void main() {
	String name = "General the Jaguar.";
	IO.println(name.length());
}
```

```
Output:
19
```

### isEmpty
`isEmpty` returns a boolean showing if the string is empty.
```java,runnable,strings_3
void main() {
	String name = "";
	IO.println(name.isEmpty()); // true
}
```

```
Output:
true
```

### Contains
`contains` returns a boolean showing if the string contains some specified value.
```java,runnable,strings_4
void main() {
	String name = "General the Jaguar.";
	IO.println(name.contains("Jaguar")); // true
}
```

```
Output:
true
```

### toLowerCase and toUpperCase
`toLowerCase` and `toUpperCase` returns a new string with the characters changed to either lower or upper case.
```java,runnable,strings_5
void main() {
	String name = "General the Jaguar.";
	IO.println(name.toUpperCase());
	IO.println(name.toLowerCase());
}
```

```
Output:
GENERAL THE JAGUAR.
general the jaguar.
```

## String Comparison
A String is an object (introduced later, but just keep in mind) and because of that, the `==` operator usually does NOT compare the contents of the string.

Sometimes, we need to use `new` (also introduced later) to create a new object in Java. Notice what happens when we try to compare the two using `==`.

We find that it returns false. This is because `x` and `y` are two distinct *objects* that Java creates separately. When Java creates an object, is places it at some memory location. So, when using `==`, we are actually comparing memory locations and not what is in that location.

```java,runnable,strings_6
void main() {
	String x = new String("Hello.");
	String y = new String("Hello.");
	IO.println(x == y); // false
}
```

```
Output:
false
```

To compare the **contents** of a string, we use the `equals` method (or `equalsIgnoreCase` for ignoring capitalization differences).

```java,runnable,strings_7
void main() {
	String x = new String("Hello.");
	String y = new String("Hello.");
	IO.println(x.equals(y)); // true
}
```
```
Output:
true
```
