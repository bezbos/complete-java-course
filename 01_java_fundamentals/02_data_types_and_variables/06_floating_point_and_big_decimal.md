
In this section, we'll cover floating-point primitives, used for representing decimal numbers.

## Float Primitive

The `float` primitive takes up 32 bits of memory to represent decimal numbers, accurate up to 7 decimal digits:
```java
float floatValue = 1.1234567F;
```

Float values must be suffixed with `F`, or you will encounter a compilation error. 
This is because all floating-point numbers in Java are considered as doubles by default, and doubles take up 64 bits.

Minimum and maximum float values:
```java
float minFloat = Float.MIN_VALUE;
float maxFloat = Float.MAX_VALUE;
System.out.println("Minimum Float: " + minFloat);
System.out.println("Maximum Float: " + maxFloat);
```

## Double Primitive
The `double` primitive takes up 64 bits of memory to represent decimal numbers, accurate up to 17 decimal digits:
```java
double doubleValue = 1.123456789012345;
```

Doubles can be suffixed with `D`, but it’s not mandatory.

Minimum and maximum double values:
```java
double minDouble = Double.MIN_VALUE;
double maxDouble = Double.MAX_VALUE;
System.out.println("Minimum Double: " + minDouble);
System.out.println("Maximum Double: " + maxDouble);
```

## Monetary calculations
Floating-point data types are not recommended for monetary calculations due to rounding issues. 
Instead, use the `BigDecimal` data type, which can preserve any amount of precision and supports "_Banker’s rounding._"

Example using BigDecimal:
```java
import java.math.BigDecimal;

BigDecimal bd1 = BigDecimal.valueOf(1.0000000000000000000015);
BigDecimal bd2 = BigDecimal.valueOf(0.000000000000000000001);
System.out.println(bd1.add(bd2));
```

Although `BigDecimal` is not a primitive data type, it's commonly used for precise calculations.