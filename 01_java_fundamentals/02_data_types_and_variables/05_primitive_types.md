At the core of every programming language are the _primitive data types_, including integers, floating-point numbers, characters, and booleans. 
_Reference data types_ represent objects and function differently.

## Primitive Number Types

### Byte `byte`

The smallest number primitive, taking 8-bits of memory and representing a number between -128 and 127:

```java
byte byteNumber = 100;
```

### Short `short`
The `short` number primitive takes up 16-bits of memory:

```java
short shortNumber = 20000;
short minShort = Short.MIN_VALUE;
short maxShort = Short.MAX_VALUE;
System.out.println("Minimum Short: " + minShort);
System.out.println("Maximum Short: " + maxShort);
```

### Integer `int`
The `integer` number primitive takes up 32-bits of memory:

```java
int intNumber = 1_200_300;
int minInt = Integer.MIN_VALUE;
int maxInt = Integer.MAX_VALUE;
System.out.println("Minimum Integer: " + minInt);
System.out.println("Maximum Integer: " + maxInt);
```

### Long `long`
The "long" number primitive takes up 64-bits of memory to represent very large numbers:

```java
long longNumber = 100_200_300_400L;
long minLong = Long.MIN_VALUE;
long maxLong = Long.MAX_VALUE;
System.out.println("Minimum Long: " + minLong);
System.out.println("Maximum Long: " + maxLong);
```

When declaring longs, apply the `L` suffix to avoid compilation errors.

### Unsigned Integers
Java doesn't have unsigned integers; use the `long` primitive for the maximum unsigned integer value.

### Boolean `boolean`
The `boolean` primitive represents `true` or `false`:

```java
boolean isAccountEnabled = true;
boolean isAccountExpired = false;
```

### Character `char`
The character `char` primitive takes up 16-bits and represents a single Unicode character from the UTF-16 table:

```java
char letterA = 'a';
char number1 = '1';
char greekLetterGamma = 'Γ';
char electricitySign = '⚡';
System.out.println(letterA + " " + number1 + " " + greekLetterGamma + " " + electricitySign);
```

Characters in Java must be surrounded by single-quotation marks.