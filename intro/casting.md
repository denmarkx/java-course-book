# Type Casting
**Type Casting** refers to switching the data type of a variable.

There are two types of casting: **implicit** and **explicit**.

## Implicit Casting
Implicit casting can occur when a data type is *smaller* than the new data types. For example, an `int` is smaller than a `double`. 

This is done by just declaring the data type and assigning it to the old variable:
```java,runnable,casting_0
void main() {
	int x = 10; // x = 10
	double y = x; // y = 10.0
	IO.println(y);
}
```

```
Output:
10.0
```

## Explicit Casting
Explicit casting refers to manually writing the type you want to cast to. This is used when you want to convert a larger data type into a smaller one.

For instance, a `double` is larger than an `int`. If we convert a `double` to an `int`, we will lose the decimal values.

This is done by placing the type in parenthesis in front of the value:

```java,runnable,casting_1
void main() {
	double x = 99.43;
	int y = (int) x;
	IO.println(y);
}
```
```
Output:
99
```
