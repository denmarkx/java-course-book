# If and Else
Let's say we wanted to print out text *only if* some condition is met. We use what is called an **if statement**.

For example, if the sky is blue, we'll print out "The sky is blue today". For this, we use the `if` keyword.

```java,runnable,ifelse_0
void main() {
	boolean isSkyBlue = true;

	// equivalent to if (isSkyBlue == true)
	if (isSkyBlue) {
		IO.println("The sky is blue today.");
	}
}
```

```
Output:
The sky is blue today.
```

The properly terminology for this if statement is called a **conditional statement**. The `isSkyBlue` piece inside that statement is called our **predicate**. 

The predicate is always some boolean value. In this case, `isSkyBlue` is true. Knowing that, we can apply any logical or comparison operator:

```java,runnable,ifelse_1
void main() {
	boolean isSkyBlue = false;

	// equivalent to if (isSkyBlue == false)
	if (!isSkyBlue) {
		IO.println("The sky is NOT blue today.");
	}
}
```

```
Output:
The sky is NOT blue today.
```

The statement `if (!isSkyBlue)..` is read literally as "if NOT is sky blue". In proper English we read it as "if the sky is NOT blue".

## Else
Let's say we wanted to combine the previous two examples. If the sky is blue, we print out "The sky is blue today". If the sky is not blue, we print out "The sky is NOT blue today". 

For this, we can use the `else` keyword.

A good way to read `else` is reading it as "otherwise".

```java,runnable,ifelse_2
void main() {
	boolean isSkyBlue = true;

	// equivalent to if (isSkyBlue == true)
	if (isSkyBlue) {
		IO.println("The sky is blue today.");
	} else { // isSkyBlue == false
		IO.println("The sky is NOT blue today.");
	}
}
```

```
Output:
The sky is blue today.
```

## Else If
Define: `char grade = 'A';`.

Let's say we have multiple conditions and want to print different things out according to those conditions:
* Grade 'A' → "Awesome!" 
* Grade 'B' → "Cool!"
* Grade 'C' → "Fair.."
* ..anything else → "Oh no!"

We can use an `if else` statement:

```java,runnable,ifelse_3
void main() {
	char grade = 'B';

	if (grade == 'A') {
		IO.println("Awesome!");
	} else if (grade == 'B') {
		IO.println("Cool!");
	} else if (grade == 'C') {
		IO.println("Fair..");
	} else {
		IO.println("Oh no!");
	}
}
```

```
Output:
Cool!
```

## Nested If and Else
If and Else can be nested. Consider the following scenario.

We have a boolean `inStock`, a double `customer_balance`, and `item_price`. We want to print out things depending on if the item is in stock as well as if the customer has enough to pay for the item:

![If Else Flow Chart](../images/FlowChart_IfElse.png)

The code is as follows:
```java,runnable,ifelse_4
void main() {
	boolean inStock = true;
	double customer_balance = 100.32;
	double item_price = 74.99;

	// Check if item is in stock..
	if (inStock) {
		// It is.
		// Check if customer has enough:
		if (customer_balance >= item_price) {
			IO.println("Payment successful!");
		} else {
			IO.println("Insufficient funds.");
		}
	} else {
		IO.println("Item is out of stock.");
	}
}
```

```
Output:
Payment successful!
```

## Logical Operators
We can also use logical operators to define the predicate. For example, let's have two booleans: `isWeekend` and `isSunny`.

Now, let's define our predicates and outputs:
* If it's the weekend *and* it is sunny → "It's a beautiful weekend!"
* If it's *not* the weekend *and* it is sunny → "It's a beautiful weekday!"
* If it's the weekend *and* it is *not* sunny → "I should stay inside today."
* If it's *not* the weekend *and* it is *not* sunny → "I'm not going to work today."

We can write the code as:
```java,runnable,ifelse_5
void main() {
	boolean isWeekend = false;
	boolean isSunny = false;

	if (isWeekend && isSunny) {
		IO.println("It's a beautiful weekend!");
	} else if (!isWeekend && isSunny) {
		IO.println("It's a beautiful weekday!");
	} else if (isWeekend && !isSunny) {
		IO.println("I should stay inside today.");
	} else if (!isWeekend && !isSunny) {
		IO.println("I'm not going to work today.");
	}
}
```
```
Output:
I'm not going to work today.
```
