If you try casting strings into numbers and vice-versa, you’ll notice that it doesn’t work:

```java
String string = "10";
int number = (int) string; // this won’t work
```

Neither will this:

```java
int number = 10;
String string = (String) number;
```

To convert between strings and numbers, use conversion methods. In Java, every primitive type has an equivalent reference type. 
For example, the `Integer` class has useful methods for converting integers into binary or hexadecimal strings. 
To read strings as numbers:

```java
String string = "10";
Integer number = Integer.parseInt(string);
```

This method can only parse valid numbers; otherwise, it throws a `NumberFormatException`.

Other number classes have almost identical parse methods:

```java
Byte.parseByte("10");
Short.parseShort("10");
Integer.parseInt("10");
Long.parseLong("10");
Float.parseFloat("3.14");
Double.parseDouble("3.14");
```

To convert numbers into strings, use the `valueOf()` method on the `String` class:

```java
String.valueOf(10);
String.valueOf(100_000_000_000L);
String.valueOf(3.14f);
String.valueOf(3.14);
```

You can also convert between booleans and strings:

```java
Boolean.parseBoolean("true");
String.valueOf(true);
```

Another common way is string concatenation:

```java
String stringTen = 10 + "";
String stringTrue = true + "";
```

When adding a number and a string, Java converts the number into a string. However, order of operations matters:

```java
String string = 10 + 20 + 30 + "";
System.out.println(string);
// Prints 60

String string = "" + 10 + 20 + 30;
System.out.println(string);
// Prints 102030
```