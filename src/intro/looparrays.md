# Looping
We can use the `for` loop and the `length` property to iterate through the array. (Another term for "iterating through the array" is called *traversing*).

```java,runnable,looparrays_0
void main() {
	int[] even = {2, 4, 6, 8, 10};

	for (int i = 0; i < even.length; i++) {
		IO.println(even[i]);
	}
}
```

```
Output:
2
4
6
8
10
```

## For-Each Looping
Another short-hand way to traverse through an array is to write the for loop statements in a "for-each" manner. This bypasses the index portion of the for loop.

```
for (<data type> <variable> : <array variable>) {
	// <code block>
}
```

As an example:
```java,runnable,looparrays_1
void main() {
	int[] even = {2, 4, 6, 8, 10};

	// Using a regular for loop.
	for (int i = 0; i < even.length; i++) {
		IO.println(even[i]);
	}

	// Using the for-each way:
	for (int x : even) {
		IO.println(x);
	}
}
```

```
Output:
2
4
6
8
10
2
4
6
8
10
```

A good way to read the following: `for (int x : even)` is: "for each element `x` in (`:`) the even array..".