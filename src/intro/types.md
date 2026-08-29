# Data Types
Java is what we refer to as a **statically typed** language. Meaning, you must explicitly write out the data type for variables, functions, etc.

We can divide data types into two groups: **primitive** and **non-primitive** types.

## Primitive Data Types
**Primitive** data types are the foundational types. Java has (roughly) 8 primitive data types.

| Data Type | Description |
| --------- | ----------- |
| byte      | Whole Numbers: [-128, 127]        |
| short     | Whole Numbers: [-32768, 32767]        |
| int       | [-2.1m, 2.1m]        |
| long      | Large Whole Numbers       |
| float     | Fractional Numbers (6-7 decimal digits)        |
| double    | Fractional Numbers (15-16 decimal digits)        |
| boolean   | True or False        |
| char      | A single character (letter) or an ASCII value.        |

### Numbers
When NOT working with anything involving low-level or requiring high performance, an `int` usually suffices rather than using `byte` or `short`.

#### Long
When dealing with numbers that are larger than what an `int` can hold, we use `long`. The number here ends with the value `L`:

```java
void main() {
    long x = 9999999999L;
    IO.println(x);
}
```

```
Output:
9999999999
```

### Floats and Doubles
When you need a number with a decimal, you use either `float` or `double` and append either an `f` or `d`, respectively:

```java,runnable,types_0
void main() {
    float x = 1.23f;
    IO.println(x);

    double y = 19.89d;
    IO.println(y);
}
```

```
Output:
1.23
19.89
```

### Booleans
A boolean is either `true` or `false`.

```java
boolean isCSCI1437 = true;
```

### Characters
A `char` is used to store a single character and uses single quotes (`''`):

```java
char day = 'W';
```

## Non-Primitive Data Types
**Non-primitive** data types are types that are more complex and built out of several primitive types. One example is a **String**. These usually have their first letter capitalized.

In reality, a string is just an array of characters (which is why we call a string non-primitive).

A String uses double quotes (`""`).
```java,runnable,types_1
void main() {
    String name = "General the Jaguar";
    IO.println(name);
}
```
```
Output:
General the Jaguar
```
