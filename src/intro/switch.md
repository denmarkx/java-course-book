# Switch Cases
Consider the example from the "If and Else" section:

```java,runnable,switch_0
void main() {
    char grade = 'B';

    if (grade == 'A') {
        IO.println("Awesome!");
    } else if (grade == 'B') {
        IO.println("Cool!");
    } else if (grade == 'C') {
        IO.println("Fair..");
    } else {
        IO.println("Oh no!");
    }
}
```

```
Output:
Cool!
```

Instead of having several if and else statements, we can use a `switch` statement instead and break down grade letters A, B, and C into "cases" using the `case` keyword.

Before writing the full thing, let's look at when the grade letter is A or if it is NOT A, B, or C.

```java,runnable,switch_1
void main() {
    char grade = 'A';

    switch (grade) {
        // Equivalent to: if (grade == 'A')
        case 'A':
            // ..then
            IO.println("Awesome!");

            // We use a break statement here to stop the switch after we found the matching case.
            break;

        // Equivalent to: else. Meaning grade does not match with any of the cases.
        default:
            IO.println("Oh no!");
            break;
    }
}
```

```
Output:
Awesome!
```

Knowing that, our full switch statement is:
```java,runnable,switch_2
void main() {
    char grade = 'A';

    switch (grade) {
        // Equivalent to: if (grade == 'A')
        case 'A':
            // ..then
            IO.println("Awesome!");

            // We use a break statement here to stop the switch after we found the matching case.
            break;

        case 'B':
            IO.println("Cool!");
            break;

        case 'C':
            IO.println("Fair..");
            break;

        // Equivalent to: else. Meaning grade does not match with any of the cases.
        default:
            IO.println("Oh no!");
            break;
    }
}
```

```
Output:
Awesome!
```

## Strings and Many Cases to One Output
We can also do switch statements on a String.

```java,runnable,switch_3
void main() {
    String day = "Monday";
    switch (day) {
        case "Monday":
            IO.println("We do not meet on Mondays.");
            break;
        default:
            IO.println("Perhaps we meet today?");
    }
}
```

```
Output:
We do not meet on Mondays.
```

Additionally, we can do multiple cases that give out a common output:

```java,runnable,switch_4
void main() {
    String day = "Thursday";

    switch (day) {
        case "Monday":
            IO.println("We do not meet on Mondays.");
            break;

        case "Tuesday", "Thursday":
            IO.println("We meet today!");
            break;

        default:
            IO.println("We do not meet today.");
    }
}
```

```
Output:
We meet today!
```

## Value of a Switch Statement
Switch statements can return values and be assigned to a variable. For this, we use the `yield` keyword.

```java,runnable,switch_5
void main() {
    String day = "Monday";

    int dayNum = switch (day) {
        case "Sunday": yield 0;
        case "Monday": yield 1;
        case "Tuesday": yield 2;
        case "Wednesday": yield 3;
        case "Thursday": yield 4;
        case "Friday": yield 5;
        case "Saturday": yield 6;
        default: yield -1;
    };

    IO.println(dayNum);
}
```

```
Output:
1
```

## Java 14+
Java 14+ uses a modern approach toward switch statements.
* No need for the `break` keyword.
* Colons after the case changes to an arrow `->`

For example: we can rewrite the grade letter example as the following:

```java,runnable,switch_6
void main() {
    char grade = 'A';

    switch (grade) {
        case 'A' -> IO.println("Awesome!");
        case 'B' -> IO.println("Cool!");
        case 'C' -> IO.println("Fair..");
        default -> IO.println("Oh no!");
    }
}
```

```
Output:
Awesome!
```

This is just a different way of writing the switch statement. It does not change the behavior at all.