# Loop Flow
There are two primary ways to control the flow of the loop while it is in progress: **break** and **continue**.

## Break
An easy way to read `break` is if you want to "break out of the loop" and stop it from progressing at a certain point.

For example, if we were looping through the first 10 integers starting from 0, but want to stop at 7:

```java,runnable,loopflow_0
void main() {
	for (int i=0; i < 10; i++) {
		if (i == 7) {
			break;
		}
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
```

## Continue
**Continue** is used if we want to *skip* an iteration.

For example, under the same scenario, let's skip the number 7 only.

```java,runnable,loopflow_1
void main() {
	for (int i=0; i < 10; i++) {
		if (i == 7) {
			continue;
		}
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
8
9
```
