# Fixed Arrays

**Arrays** are used to store multiple values in a single variable. For now, we are going to talk about a **fixed** array.

**Fixed Arrays** are *fixed* because their **size** cannot change at runtime. The values are able to be changed.

## Array Definition
For arrays, we use the variable type and square brackets (`[]`). For the values within the array, we wrap them inside curly braces (`{}`). You may also hear the values within an array being called "elements".

There are several ways to define an array. The simplest is without an explicit size:

To declare an array, without an explicit size:
```java
void main() {
	int[] even = {2, 4, 6, 8, 10};
}
```

To declare an array with an explicit size and without any values, we can use the `new` keyword:
```java
void main() {
	// New integer array that has enough space for five integers.
	int[] even = new int[5];
}
```

## Accessing Elements
An array can be accessed through **indices**. In an array, an index is the "location" (starting at 0) of some element. 

Looking back at the `evens` array example:

```java
void main() {
	int[] even = {2, 4, 6, 8, 10};
}
```

There are five elements. Each element is located at an index. The first index of an array always starts at zero.

| Value | Index |
| ----- | ----- |
| 2 | 0 |
| 4 | 1 |
| 6 | 2 |
| 8 | 3 |
| 10 | 4 |

To access the array, we use square brackets (`[<index>]`). To get the number value at index 2, we write: `even[2]`:

```java,runnable,arrays_0
void main() {
	int[] even = {2, 4, 6, 8, 10};
	IO.println(even[2]); // 6
}
```

```
Output:
6
```

## Changing Elements
Consider the example where we used `new`:
```java
void main() {
	int[] even = new int[5];
}
```

There exists 5 "placeholder" elements within this array. We can change that placeholder into a value by using square brackets and assigning it to some value:

```java,runnable,arrays_1
void main() {
	int[] even = new int[5];
	even[0] = 2;
	even[1] = 4;
	even[2] = 6;
	even[3] = 8;
	even[4] = 10;
}
```

Even after we changed the placeholder (or if we created the array without `new`), we can still continue to switch out the element:
```java,runnable,arrays_2
void main() {
	int[] even = {2, 4, 6, 8, 10};
	even[3] = 82;

	// Our array is now: {2, 4, 6, 82, 10};
	IO.println(even[3]); // 82
}
```

```
Output:
82
```

## Length
To get the length of an array, we can use the `length` **property** (introduced later, but what you need to know is that a property is not callable).

`length` will return the size of the array starting from 1.

```java,runnable,arrays_3
void main() {
	int[] even = {2, 4, 6, 8, 10};
	IO.println(even.length); // 5
}
```

```
Output:
5
```
