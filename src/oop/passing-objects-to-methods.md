# Passing Objects to Methods
> [!IMPORTANT]
> Please review what a [primitive type](/intro/types.html#primitive-data-types) is before continuing.

Strictly speaking, there is only one way to pass data to methods: **pass-by-value**. However, there is a special form of this called **pass-by-sharing** that is sometimes described as Java's second way to pass data to methods.

## Pass-by-Value
Pass-by-Value means a **copy** of the data is created. Any changes done to that variable is done to the copy and not the original variable.

Primitive types are always passed-by-value.

```java
void display(int num) {
	// <num> is a copy of x.
	num += 1;
}

void main() {
	int x = 10;

	display(x);
	IO.println(x);
}
```

```
Output:
10
```

## Pass-by-Sharing
Pass-by-Sharing means we pass a **reference** that refers to the original object. Any changes done to that reference variable will be applied to the same object.

```java
class Animal {
	public String name;

	public Animal(String name) {
		this.name = name;
	}
}

void change(Animal animal) {
	// <animal> refers to the original animal object.
	animal.name = "Rubble";
}

void main() {
	Animal animal = new Animal("Rocky");

	// We pass our reference variable:
	change(animal);
	IO.println(animal.name);
}
```

```
Output:
Rubble
```

> [!NOTE]
> If we were speaking in a strict sense, Java has only one way to pass values: pass-by-value. 
> 
> Applying that logic to our example above, what actually happens is we pass a **copy of the reference variable** to our change method.
>
> Since it is a copy of a reference variable, that copy **still refers to the same object** which is why you may sometimes hear this called pass-by-value.

### Improper Example
Consider the following code below and its output.

```java
void change(Animal animal) {
	animal = new Animal("Rubble");
}

void main() {
	Animal animal = new Animal("Rocky");
	change(animal);
	IO.println(animal.name);
}
```

```
Output:
Rocky
```

The output here is "Rocky" because even though we pass-by-sharing, we are actually **overwriting our parameter in the change method**. 

Recall, a parameter is still a local variable. So we are actually reassigning that local variable to a new animal object.