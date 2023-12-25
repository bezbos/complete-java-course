Java is a _statically-typed_ language, meaning variables and methods have strictly defined data types. Consider the following:

```java
int a = 2; // Assigning a string to this variable would not work
a = "two";
```

To assign a string, declare a variable of type String:

```java
String str = "two";
```

Java enforces _type-safety_ during compile-time, preventing mismatches between variable types and values. Unlike languages 
like JavaScript or Python, which are dynamically typed and allow indiscriminate value assignments:

```python
foo = 2
foo = "bar"
```

While dynamic typing can be convenient, it poses safety risks. Java 10 introduced the `var` type name, providing some dynamic 
typing convenience:

```java
var foo = "bar";
```

Used for local variables within methods, `var` enhances code readability without affecting runtime performance. It's essential 
to note that `var` cannot be used for class member variables or method parameters.

```java
public class Application {
    // This won't work
    var foo = "bar";

    // Neither will this
    public static void main(var args) {...}
}
```

For class members and parameters, explicit variable type declaration is necessary.

The motivation behind `var` is to make code cleaner by eliminating data type repetition. Although it's been present in Java, 
it's underused due to old habits. Embracing `var` enhances code readability without performance penalties, making it a valuable 
addition to modern Java codebases.