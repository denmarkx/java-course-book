# Input and Output

## Output
To write some output to the terminal, we use the function `IO.println`. Internally, `println` will append a newline character `\n` signifying that the line has ended.

To print some text without a newline, we use `IO.print`.

```java,runnable,syntax_0
void main() {
    IO.print("Hello ");
    IO.println("World!");
}
```

```
Output:
Hello World!
```

### Formatting
To place some variable within a string, we can use `.formatted` alongside some **format specifier**.

```java
void main() {
    String name = "General the Jaguar";
    IO.println("My name is %s.".formatted(name));
}
```

The general syntax for format specifiers is:
```
%[flags][width][.precision]conversion
```

Common values for `conversion` are the following:

| Conversion | Data Type |
| ---------- | --------- |
| `b` | `boolean` |
| `c` | `char` |
| `d` | `int` |
| `e` | Scientific Notation |
| `f` | `double` |
| `s` | `string` |

Common values for `flag` are the following:

| Flag | Description |
| ---- | ----------- |
| `-` | Left justification |
| `+` | include positive sign |
| `0` | pad with zeros |

The `width` is the total number of characters that the portion of the string will contain.

The `precision` determines thenumber of digits to the right of the decimal point.

#### Example:
```java
void main() {
    double pi = Math.PI;

    IO.println("%f".formatted(pi));
    IO.println("%.2f".formatted(pi));
    IO.println("%.4f".formatted(pi));
    IO.println("%.10f".formatted(pi));
    IO.println("%10.2f".formatted(pi));
    IO.println("%-10.2f".formatted(pi));
    IO.println("%010.2f".formatted(pi));
    IO.println("%e".formatted(pi));
    IO.println("%.3e".formatted(pi));
    IO.println("|%-12.3f|".formatted(pi));
}
```

```
Output:
3.141593
3.14
3.1416
3.1415926536
      3.14
3.14      
0000003.14
3.141593e+00
3.142e+00
|3.142       |
```

### Breakdown
```java
void main() {
    double pi = Math.PI;
    IO.println("%+012.4f".formatted(pi));
}
```

```
Output:
+000003.1416
```

We can breakdown the pattern `%+012.4f` as so:
```
% + 0 12 .4 f
  │ │ │  │  │
  │ │ │  │  └── floating-point
  │ │ │  └───── 4 digits after decimal
  │ │ └──────── padding width of 12
  │ └────────── zero padding
  └──────────── show + for positive
```

## Input
To accept input from the console, we use the `IO.readln(<message>)` function:

```java
void main() {
    String input = IO.readln("Please enter your name: ");
    IO.println("Your name is: " + input + "!");
}
```

```
Output:

Please enter your name: General the Jaguar
Your name is: General the Jaguar!
```

Anything we receive from `readln` will always be a String:
```java
void main() {
    String input = IO.readln("Please enter a number: ");

    // Since <input> is a string, we CANNOT perform mathematical operations.
    // input + 5: <String> + <int>
}
```

Thus, we must convert the String to some value:
```java
void main() {
    String input = IO.readln("Please enter a number: ");
    
    int number = Integer.parseInt(input);
    int numberSquared = number * number;

    IO.println("Number squared is: %d.".formatted(numberSquared));
}
```

```
Output:

Please enter a number: 5
Number squared is: 25.
```