In Java, errors are categorized into two types: compile-time errors and runtime errors. This lesson focuses on compile-time 
errors, which occur before the program is executed. The Java compiler attempts to translate the Java source code into JVM 
bytecode during this phase.

If the compiler encounters errors, it halts the compilation process and provides a report indicating the location of the 
error, including the file and line number. The program cannot be run until all compile-time errors are resolved.

## Common Compile-time Errors

1. **Syntax errors:** These occur when the Java language syntax rules are violated. Examples include missing semicolons, mismatched parentheses or curly braces, and incorrect keyword usage.

2. **Type errors:** These occur when attempting to assign a value of one data type into a variable of a different data type (e.g., assigning a string value to an integer variable).

3. **Referencing undefined symbols:** Trying to read or write into a variable that doesn’t exist.

4. **Access control errors:** Occur when attempting to access a variable, method, or class from a location in the code where access is restricted by access modifiers like `private`, `protected`, or `package-private`. Detailed coverage of access modifiers will be discussed in the next part of the course, Java OOP.

5. **Missing return statements:** In methods that are expected to have a return value.

Most Java compile-time errors are easily fixable and, crucially, can be resolved before the program runs.
