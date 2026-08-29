# Multidimensional Arrays
A **multidimensional array** is an array that contains other arrays. A good example of this is a table.

To create a two-dimensional array we can write:
```java
void main() {
	int[][] nums = {
// Col.   0  1  2  3 
		{ 2, 4, 6, 8 }, // Row 0
		{ 1, 3, 5, 7 }, // Row 1
	};
}
```

## Accessing Elements
To access an element of a 2D array, we must supply two indices: one for the *row* and the other for the *column*.
```java,runnable,multidimen_0
void main() {
	int[][] nums = {
// Col.   0  1  2  3 
		{ 2, 4, 6, 8 }, // Row 0
		{ 1, 3, 5, 7 }, // Row 1
	};

	IO.println(nums[1][2]); // -> 5
}
```

```
Output:
5
```

## Looping
To loop through our 2D array, we can write a nested for loop:
```java,runnable,multidimen_1
void main() {
	int[][] nums = {
// Col.   0  1  2  3 
		{ 2, 4, 6, 8 }, // Row 0
		{ 1, 3, 5, 7 }, // Row 1
	};

	// First loop: row iteration (row 0 or 1):
	for (int i=0; i < nums.length; i++) {
		// Second loop: column iteration (cols. 0, 1, 2, 3):
		for (int j=0; j < nums[i].length; j++) {
			IO.println(nums[i][j]);
		}
	}
}
```

```
Output:
2
4
6
8
1
3
5
7
```

..alternatively, a for-each loop can still be used:
```java,runnable,multidimen_2
void main() {
	int[][] nums = {
// Col.   0  1  2  3 
		{ 2, 4, 6, 8 }, // Row 0
		{ 1, 3, 5, 7 }, // Row 1
	};

	// First loop: row iteration (row 0 or 1):
	for (int[] row : nums) {
		// Second loop: column iteration
		for (int num : row) {
			IO.println(num);
		}
	}
}
```

```
Output:
2
4
6
8
1
3
5
7
```
