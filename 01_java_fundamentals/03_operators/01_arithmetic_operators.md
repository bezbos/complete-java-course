## Arithmetic Operators

Arithmetic operators are fundamental for performing operations like addition, subtraction, multiplication, and division on numeric values.

### Addition

Use the addition operator to add two numbers:

```java
int addition = 2 + 4;
System.out.println("2 + 4 = " + addition);
```

### Subtraction
For subtraction:

```java
int subtraction = 4 - 2;
System.out.println("4 - 2 = " + subtraction);
```

### Multiplication
To multiply numbers:

```java
int multiplication = 4 * 4;
System.out.println("4 * 4 = " + multiplication);
```

### Division
Perform division:

```java
int division = 8 / 2;
System.out.println("8 / 2 = " + division);
```

Be cautious about division by zero, as it results in an exception:

```java
int divisionByZero = 8 / 0;
System.out.println("8 / 0 = " + divisionByZero);
```

### Modulo
Obtain the remainder of a division using the modulo operator:

```java
int divisionRemainder = 5 % 2;
System.out.println("5 / 2 remainder = " + divisionRemainder);
```

Modulo is useful for checking if a number is odd or even.

## Combined Assignment Operators
Simplify arithmetic operations with assignment:

```java
int x = 50;
int y = 20;
x += y; // Equivalent to x = x + y;
System.out.println(x); // Outputs 70
```

Combined assignment forms exist for subtraction, multiplication, division, and modulo.

```java
x -= y;
x *= y;
x /= y;
x %= y;
```

## Unary Arithmetic Operators
Unary operators are shortcuts for incrementing and decrementing variables, commonly used in loops.

### Unary Increment
```java
int u = 5;
System.out.println(u++); // Outputs 5
System.out.println(u);   // Outputs 6
System.out.println(++u); // Outputs 7
```

The two variants increment the variable differently.

### Unary Decrement
```java
System.out.println(u--); // Outputs 7
System.out.println(u);   // Outputs 6
System.out.println(--u); // Outputs 5
```