# For Loop
Let's say we wanted to print out the numbers 0 through 5 (non-inclusive). 

We could write:

```java,runnable,for_0
void main() {
	IO.println(0);
	IO.println(1);
	IO.println(2);
	IO.println(3);
	IO.println(4);
}
```

```
Output:
0
1
2
3
4
```

This gets a bit cumbersome when we want to print the numbers 0 through 20 (non-inclusive). For that, we can use a **for loop**.

A for loop's structure is as follows:
```
for (<statement 1>; <statement 2>; <statement 3>) {
	// <code block>
}
```

Where:
* Statement 1 is executed once *before* the code block.
* Statement 2 defines the predicate for executing the code block.
* Statement 3 is executed every time *after* the code block.

Knowing that, we can write our for loop for print numbers 0 to 20 (non-inclusive) as follows:

```java,runnable,for_1
void main() {
	for (int i=0; i < 20; i++) {
		IO.println(i);
	}
}
```

```
Output:
0
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
```

We can read our code as: "starting at `i=0`, increment `i` by one (`i++`) and execute `IO.println` *until* `i < 20`".


We can use this to do all sorts of things. For example, the sum of numbers 1 to 10 (inclusive):

```java,runnable,for_2
void main() {
	int sum = 0;
	for (int i = 1; i <= 10; i++) {
		sum = sum + i;
	}
	IO.println(sum);
}
```
```
Output:
55
```
