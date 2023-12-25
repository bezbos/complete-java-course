In Java, values assigned to primitive data type variables are called **literals**. These are fixed values interpreted from source code without computation. Examples include: `2`, `3.14`, `"foo"`, or `true`.

### Binary and hexadecimal forms

```java
int binaryValue = 0b10101; // 21 in binary
int hexadecimalValue = 0x15; // 21 in hexadecimal
System.out.println(binaryValue);
System.out.println(hexadecimalValue);
```

Print numbers in binary or hexadecimal:
```java
System.out.println(Integer.toBinaryString(21));
System.out.println(Integer.toHexString(21));
```

### Scientific notation:

```java
float scientificFloat = 3.24e3f;
double scientificDouble = 1.234e2;
System.out.println(scientificFloat);
System.out.println(scientificDouble);
```

### Readable Big Number Literals
Use underscores `_` for readability:

```java
long creditCardNumber = 4024_0071_6728_7548L;
System.out.println(creditCardNumber);
```

Underscores are ignored and can be applied in hexadecimal and binary representations.

#### Caution with Underscores
Be careful where you place underscores:

```java
int badLiteral1 = 123_;, int badLiteral2 = _123; // Incorrect
float badLiteral3 = 3._12F; // Incorrect
long badLiteral4 = 1000_L; // Incorrect
int badLiteral5 = 0_x32; // Incorrect
```

Mistakes are easily spotted by the compiler and can be fixed.

### Special Literals

#### Null Literal
   ```java
   String name = null; // Absence of an object handle
   System.out.println(name);
```
#### Class Literal:
```java
Class cl = String.class; // Refers to the object representing the type itself
System.out.println(cl);
```