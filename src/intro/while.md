# While Loop
Alternatively, we can use a **while loop** which has the syntax of:

```
while (<condition>) {
	<code block>
}
```

Which can be read as: "while the condition is true, execute the code block".

The condition is updated within the code block. For example, printing out numbers 0 to 4 (inclusive):

```java,runnable,while_0
void main() {
	int i = 0;

	// While i is less than 5:
	while (i < 5) {
		IO.println(i);
		i++; // Increment i by 1.
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
```

At the beginning, `i=0`. On the next loop, `i=1`, then 2, 3, 4, and stopping when `i=5` because `5 < 5 = False`.

> **Note**: It is important that you remember to update the condition inside the while loop! Otherwise, the loop will repeat forever.

## Do-While Loops
A while loop will only start if the condition is currently true BEFORE the first loop. 

A **do-while** loop is a variant of a while loop. Even if the condition is false, the loop will run one time BEFORE testing the condition.

The syntax is as follows:

```
do {
	<code block>
} while (<condition>);
```

For example, let's have our while condition set to something that is obviously false.

```java,runnable,while_1
void main() {
	int i = 10;
	do {
		IO.println(i);
		i++;
	} while (i == 99);
}
```

```
Output:
10
```

The condition here is false to begin with. Where `i=10` and the condition is (`i == 99`). However, since this is a do-while loop, we will execute the code block *first* before checking to see if the condition is true or not.

Thus, this will run `IO.println` and print 10.