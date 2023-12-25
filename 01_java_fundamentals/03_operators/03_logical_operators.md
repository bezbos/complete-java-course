Logical operators are used for checking value equality and relations between values. These operators are most commonly used with conditional statements and loops.

Let's say we have two variables:

```java
int x = 1;
int y = 2;
```



### Equality
We can check if they're equal by using the equality operator:

```java
System.out.println("x is equal to y: " + (x == y)); // false
System.out.println("x is equal to 1: " + (x == 1)); // true
```

We have to surround the equality check with parentheses; otherwise, Java will think we're trying to compare a String with a number, which is not possible since they are different data types. For some types, Java will do automatic conversion, but it's better to explicitly convert the types to ensure accurate comparisons.

### Inequality
We can also check for inequality:

```java
System.out.println("x is not equal to y: " + (x != y)); // true
System.out.println("x is not equal to 1: " + (x != 1)); // false
```

### Greater than
We can check if one value is greater than the other:

```java
System.out.println("x is greater than y: " + (x > y)); // false
System.out.println("y is greater than x: " + (y > x)); // true
```

### Less than
We can check if one value is less than the other:

```java
System.out.println("x is less than y: " + (x < y)); // true
System.out.println("y is less than x: " + (y < x)); // false
```

### Greater than or equal
Conveniently, we can check if a value is greater than or equal to another value:

```java
System.out.println("x is greater than or equal to y: " + (x >= y)); // false
System.out.println("x is greater than or equal to 1: " + (x >= 1)); // true
System.out.println("x is greater than or equal to 0: " + (x >= 0)); // true
```

### Less than or equal
We can also check if a value is less than or equal to another value:

```java
System.out.println("x is less than or equal to y: " + (x <= y)); // true
System.out.println("x is less than or equal to 1: " + (x <= 1)); // true
System.out.println("x is less than or equal to 0: " + (x <= 0)); // false
```

### Logical NOT
When we want to invert a boolean value, we can use the logical NOT `!` operator:
```java
System.out.println(!(x == y)); // true
```

### Logical AND
When we want to check multiple conditions, we can use conditional operators. Let's say we want to check if a number is within a certain range. For this, we would use the logical AND operator:

```java
int number = 30;
System.out.println(number > 20 && number < 40);
```

So, we checked if the value of the variable "number" is between 20 and 40. Notice that for this condition to be true, both sides of the logical AND statement have to be truthy. If either one of them evaluates to false, the entire statement evaluates to false.

By the way, the term "truthy" refers to an expression that evaluates to true, and conversely, we could say "falsy" for expressions that evaluate to false.

### Logical OR
Let's say we want to check if a number is NOT within a certain range. For this, we can use the conditional OR operator:

```java
System.out.println(number > 20 || number < -20);
```

Unlike the AND operator, the OR operator will evaluate to true if at least one side is truthy. Our number is certainly not less than -20, but it is greater than 20, which causes this conditional OR statement to evaluate to true.

There is another conditional operator that is very commonly used, especially when assigning values. Let's say we want to check a condition and then get a value depending on the result. For this, we can use the ternary operator:


### Ternary operator
```java
int number = 30;
String result = number > 35 ? "is greater than 35" : "is less than 35";
System.out.println(result);
```

The ternary operator is a bit special because, unlike other operators, it's divided into three individual parts:
1. The evaluation expression
2. The value to return if the expression evaluates to `true`
3. The value to return if the expression evaluates to `false`

It might be a bit difficult to wrap your head around this operator, but don't worry about it. It will probably make more 
sense once I explain `if` statements.