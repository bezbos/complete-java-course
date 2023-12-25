We've covered all primitive types, including strings, which are technically objects used to represent text:

```java
String foo = "foo";
```

Strings are variable-sized data structures with useful methods for manipulation. For example, you can check the length of a string:
```java
System.out.println("foo length: " + foo.length());
```

To access specific characters, use `charAt(index)`. Note that indexes start at 0:


```java
System.out.println("First character of foo: " + foo.charAt(0));
System.out.println("Last character of foo: " + foo.charAt(foo.length() - 1));
```

Be cautious of index bounds to avoid exceptions. To concatenate strings, you can use the `+` operator or the `concat()` method:


```java
String foobar = "foo" + ", " + "bar" + ", " + "baz";
String foobar = foo.concat(", ").concat("bar").concat(", ").concat("baz");
```

For proper string equality comparison, use the `equals()` method:


```java
System.out.println("foo1 = foo2: " + foo1.equals(foo2));
```

Other useful string operations include:

Substring extraction:

```java
String foo = foobar.substring(0, 3);
String bar = foobar.substring(3, 6);
```

Case conversion:

```java
String foobarLowercase = foobar.toLowerCase();
String foobarUppercase = foobar.toUpperCase();
```

Searching for characters and substrings:

```java
int firstA = foobar.indexOf('a');
int lastA = foobar.lastIndexOf('a');
int startingFooIndex = foobar.indexOf("foo");
int startingBarIndex = foobar.indexOf("bar");
```

Checking if a string contains a substring:

```java
System.out.println("Contains foo: " + foobar.contains("foo"));
System.out.println("Contains bar: " + foobar.contains("bar"));
System.out.println("Contains baz: " + foobar.contains("baz"));
```

String replacement:

```java
System.out.println(foobar.replace("foo", "baz"));
System.out.println(foobar.replaceFirst("foo", "baz"));
System.out.println(foobar.replaceAll("\\.", ";"));
```

These are some of the commonly used string methods. Feel free to explore more on your own for additional practice.