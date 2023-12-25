In Java, we have multiple ways of converting values. The base mechanism for type conversion is called _casting_. 
Casting is the process of changing how a value is interpreted. For example, let's say we assign an integer to a long:

```java
int a = 10;
long b = a;
```

We don't have to do any explicit casting here because the Java compiler will implicitly cast the `int` into a `long` since
there is no danger of losing any data by casting from a smaller type into a larger capacity type.

However, if we try to assign a long into an integer, that would not work:
```java
long a = 10;
int b = a; // This code does not compile.
```

In order to make this work, we have to cast the long value into an integer:
```java
long a = 10;
int b = (int) a;
```

This is now valid code. Although, if we had cast a long that cannot fit into an integer, the excessive bits would have been cut off, and we'd get a completely different number. For example:
```java
long a = 10_000_000_000L; // This number cannot fit into an integer
int b = (int) a;
System.out.println(b);
```

This prints out a completely different number because the rightmost bits were cut off. Let's print out the variables in binary form to see what happened:
```java
System.out.println(Long.toBinaryString(a));
System.out.println(Integer.toBinaryString(b));
// a = 1001010100000010111110010000000000
// b =    1010100000010111110010000000000
```

If we align these bits, we can clearly see that 3 bits were cut off from the right side. Well, actually, 32 bits were cut off, but the `toBinaryString()` method doesn't return excessive zeroes on the right side.

So casting from smaller to larger types is done automatically:
```java
// byte -> short -> int -> long -> float -> double
byte byteValue = 127;
short shortValue = byteValue;
int intValue = shortValue;
long longValue = intValue;
float floatValue = longValue;
double doubleValue = floatValue;
```

While casting from larger to smaller types requires explicit casting:
```java
// double -> float -> long -> int -> short -> byte
double doubleValue = 3.14;
float floatValue = (float) doubleValue;
long longValue = (long) floatValue;
int intValue = (int) longValue;
short shortValue = (short) intValue;
byte byteValue = (byte) shortValue;
```