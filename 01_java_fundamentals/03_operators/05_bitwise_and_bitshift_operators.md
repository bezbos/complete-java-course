In Java, we have bitwise and bit-shift operators, useful for manipulating bits in primitive values. These are commonly 
used in low-level scenarios such as bit-masking, encryption, or binary data processing.

Consider the following variables:
```java
int bitmask = 0b0110_0011;
int value = 0b1111_0011;
```

We can apply the bitmask to the values using various operators.

## Bitwise Operators

### Bitwise AND
```java
System.out.println("value AND-ed with bitmask: " + Integer.toBinaryString(value & bitmask));
```

Each bit from the bitmask is AND-ed with the corresponding bit in the value. If both bits are `1`, the result is `1`; otherwise, it's `0`.

### Bitwise OR
```java
System.out.println("value OR-ed with bitmask: " + Integer.toBinaryString(value | bitmask));
```

If a bit on either side is `1`, the resulting bit is `1`.

### Bitwise XOR (Exclusive OR)
```java
System.out.println("value XOR-ed with bitmask: " + Integer.toBinaryString(value ^ bitmask));
```

The result is `1` only if the bits on both sides are different.

### Bitwise Complement
```java
System.out.println("value complement: " + Integer.toBinaryString(~value));
```

All bits are inverted; `1` becomes `0`, and `0` becomes `1`.

## Bit-Shift Operators

### Left Shift
```java
System.out.println("value left shift: " + Integer.toBinaryString(value << 2));
```

Shifts bits to the left by the specified number of spaces, filling empty spaces with `0`.

### Signed Right Shift
```java
System.out.println("value right shift with unset sign: " + Integer.toBinaryString(value >> 2));
System.out.println("value right shift with set sign: " + Integer.toBinaryString(~value >> 2));
```

Shifts bits to the right, filling empty spaces with `1` if the leftmost bit (sign bit) is `1`, otherwise with `0`.

### Unsigned Right Shift
```java
System.out.println("value unsigned right shift: " + Integer.toBinaryString(value >>> 2));
```

Shifts bits to the right, filling empty spaces with `0`.