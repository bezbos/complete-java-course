Arithmetic operators in Java allow basic operations like addition, subtraction, multiplication, and division. For more advanced operations such as rounding, absolute value, minimum/maximum, square roots, and logarithms, Java provides the `java.lang.Math` class with a variety of static methods.

Let's explore some examples:

```java
double a = -24.20;
double b = 31.59;
```

### Absolute Value
```java
System.out.printf("Absolute value of %f = %f%n", a, Math.abs(a));
// Result: 24.20
```

### Rounding, Flooring, and Ceiling
```java
System.out.printf("Rounded value of %f = %d%n: ", b, Math.round(b));
// Round to the nearest long value

System.out.printf("Floored value of %f = %f%n ", b, Math.floor(b));
// Round to the largest value less than or equal to it

System.out.printf("Ceiled value of %f = %f%n: ", b, Math.ceil(b));
// Round to the largest value greater than or equal to it
```

### Minimum and Maximum
```java
System.out.printf("Min value of {%f, %f} = %f%n", a, b, Math.min(a, b));
System.out.printf("Max value of {%f, %f} = %f%n", a, b, Math.max(a, b));
```

### Constants
```java
System.out.printf("Euler's number = %f%n", Math.E);
System.out.printf("PI number = %f%n", Math.PI);
```

### Exponents, Logarithms, and Powers
```java
System.out.printf("Exponent of %f = %f%n", b, Math.exp(b));
System.out.printf("Logarithm of %f = %f%n", b, Math.log(b));
System.out.printf("Square root of %f = %f%n", b, Math.sqrt(b));
System.out.printf("%f to the power of %f = %f%n", b, 2, Math.pow(b, 2));
```

### Angle Conversion and Trigonometry
```java
System.out.printf("%f radians = %f%n", b, Math.toRadians(b));
System.out.printf("%f degrees = %f%n", b, Math.toDegrees(b));

System.out.printf("Sine of %f = %f%n", b, Math.sin(b));
System.out.printf("Cosine of %f = %f%n", b, Math.cos(b));
System.out.printf("Tangent of %f = %f%n", b, Math.tan(b));
```

_Note: Trigonometric methods expect radians, not degrees._

### Random Numbers
```java
System.out.printf("Random number (0 - 1.0) = %f", Math.random());
// Returns a random double between 0.0 (inclusive) and 1.0 (exclusive)

long random = Math.round(Math.random() * 100);
System.out.printf("Random number (0 - 100) = %d", random);
// Generates a random value between 0 and 100
```