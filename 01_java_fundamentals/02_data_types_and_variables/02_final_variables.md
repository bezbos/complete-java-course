To prevent variables from being reassigned, use the `final` modifier:

```java
final double PI = 3.14;
```

The `double` data type represents fractional numbers. The final modifier prevents variable reassignment:
```java
PI = 3.1415; // Compilation error: Cannot assign a value to final variable 'PI'
```

This error ensures the prevention of reassignment, allowing the creation of constants like `PI`.

The `final` modifier is crucial for safeguarding important variables from unintended changes, providing a mechanism to 
prevent unexpected state alterations in the application.