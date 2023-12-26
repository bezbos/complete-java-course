In contrast to compile-time errors, runtime exceptions occur during the execution 
of our program, known as the program runtime.

The reason these are called "exceptions" and not "errors" is because in Java, the term "error" represents fundamental issues 
which prevent the program from being executed properly, such as compiler-errors. Errors may also happen during the execution 
of a Java program.

Examples of
errors during execution include `OutOfMemoryError` or `StackOverflowError`.

**OutOfMemoryError:**
```java
public static void main(String[] args) {
    List<Integer> list = new ArrayList<>();
    while (true) {
        list.add(1);
    }
}
```

**StackOverflowError:**
```java
public static void recursiveMethod() {
    recursiveMethod();
}

public static void main(String[] args) {
    recursiveMethod();
}
```

Even though our Java code compiles successfully, runtime errors may still crash our program. These errors are rare but may occur on resource-constrained machines, like smartphones.

### Handling Exceptions
Exceptions, representing exceptional or unexpected conditions during program execution, can be handled using `try..catch` 
blocks. For instance, if we attempt to divide by zero:

```java
double result;
try {
    // Logic that may throw an exception
    result = 1 / 0;
} catch (ArithmeticException ex) {
    // Handling the exception, informing the user, and continuing program execution
    System.out.println("You cannot divide by zero.");
}

System.out.println("Program finished.");
```

By using `try..catch`, the program doesn't crash prematurely, and we've successfully handled the exception.

I've covered the basics, but there's more to exceptions, like the difference between checked and unchecked exceptions, 
when to throw exceptions, alternative mechanisms, and advanced error handling, which require dedicated sections.