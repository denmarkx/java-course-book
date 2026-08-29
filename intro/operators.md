# Operators
An **operator** is used to perform some operation on variables and values. There are several types, but we are mainly concerned with **arithmetic**, **assignment**, **comparison**, and **logical** operators.

Operators can be used directly between values, variables, and both. They follow the standard **order of operations** used in mathematics.

```java
void main() {
	// Variable + Variable
	int x = 10;
	int y = 5;
	int sum = x + y;

	// Value + Variable
	sum = 10 + y;

	// Value + Value
	sum = 10 + 5; 
}
```

## Arithmetic Operators
Performs common math operations:

| Operator | Name | Description |
| -------- | ---- | ----------- |
| + | Addition | Adds two values |
| - | Subtraction | Subtracts two values |
| * | Multiplication | Multiplies two values |
| / | Division | Divides two values |
| % | Modulo | Division remainder |
| ++ | Increment | Increments value by 1 |
| -- | Decrement | Decrements value by 1 |

## Assignment Operators
Assigns some value to a variable:

| Operator | Description |
| -------- | ----------- |
| = | Assignment |
| += | Increment |
| -= | Decrement |
| *= | Multiply |
| /= | Divide |
| %= | Modulo |


The assignment operators involving arithmetic is a short hand way of writing code:

```java
void main() {
	int x = 5;

	// Shorter way:
	x += 10;

	// ..is the same as writing:
	x = x + 10;
}
```

## Comparison Operators
Compares two values or variables. These return a boolean.


| Operator | Description |
| -------- | ----------- |
| == | Equal to |
| != | Not equal to |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |


Example:
```java,runnable,operators_0
void main() {
	int x = 1;
	IO.println(x == 1); // true

	int y = 20;
	IO.println(x > y); // false

	IO.println(1 != 0); // true
}
```

```
Output:
true
false
true
```

## Logical Operators
Logical operators are used to combine comparison operations. These also return a boolean.

| Operator | Name | Description |
| -------- | ---- | ----------- |
| && | And | True if both statements are true. |
| \|\| | Or | True if one of the statements is true. |
| ! | Not | Returns false is statement is true. |

Example:
```java,runnable,operators_1
void main() {
	int x = 5;
	int y = 20;

	// true (both statements are true):
	IO.println(x == 5 && y == 20);

	// false: (neither statement is true).
	IO.println(x == 2 || y == 1);
}
```
```
Output:
true
false
```
