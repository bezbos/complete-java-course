An essential skill for any Java developer is debugging. Debugging is the process of identifying and fixing errors in our
code, through the use of special tools called debuggers. Debugging is essentially detective work, where you investigate 
issues, trace their causes, and make necessary corrections.

Fortunately, the JVM conditionally exposes an API that allows debugger tools to connect to our applications via the Java
Debug Wire Protocol (JDWP). This enables IntelliJ and other IDEs to provide a seamless debugging experience for developers.

### Getting Started with Debugging in IntelliJ

Debugging a Java application in IntelliJ and most other IDEs is as simple as clicking the debug button. This will run the 
application and also tell the JVM to ensure the JDWP API is exposed, so the IntelliJ debugger can connect to it.

### Setting Breakpoints

Now, let’s get started with the basics. The most fundamental feature of any debugger is the ability to set breakpoints in 
your code. If you hover over the left side margin of your editor, near the line numbers, you can click there to set a breakpoint.
This instructs the JVM to pause the process at this line. In IntelliJ, you can also press `Ctrl + F8` to set a breakpoint 
on the currently selected line.

Let’s set a breakpoint in the `divide()` method. Run the application in debug mode. The debugger has hit the breakpoint,
and we can inspect the state of the program.

During the paused state, you can execute the code line by line. On the ribbon bar, you have options for how to continue 
the execution. You can resume the program, step over the current line, or step into a method.

### Stepping into and out of Methods

Let’s try stepping into a method. Place a breakpoint on the line where we call the `divide` method, run the program in 
debug mode, and press `F7` to step into the method. You can also step out of a method using `Shift + F8`.

### Evaluating Expressions

An extremely useful feature of the debugger is the ability to evaluate expressions during the paused state. You can open
the evaluation window by clicking on the calculator-like button or pressing `Alt + F8`. This allows you to execute Java
code and test different possibilities without restarting the application.

For example:
```java
int[] numbers = {2, 3, 1};
Arrays.sort(numbers);
numbers;
```

Note that only the result of the last statement will be shown in the result view.

### Modifying Values
You can modify variable values during the paused state. For example, if you hit a breakpoint and set a variable, the execution
will reflect the change.

### Navigating the Stack Trace
You can navigate the stack trace to inspect the state of each frame individually. For each method call, a frame is added to 
the stack trace, keeping track of method calls and variables in their scope.

### Watchpoints
Watchpoints allow you to pause the program whenever a field is read or written to. You can set watchpoints on member variables
and class variables but not on local variables.

### Custom Breakpoints and Watchpoints
You can customize breakpoints and watchpoints by right-clicking on them or pressing `Ctrl + Shift + F8`. You can set a custom 
condition for triggering the breakpoint, and even set a global exception breakpoint.

---

Congratulations! You’ve just learned 99% of what you need to successfully debug Java applications. Practice makes perfect,
and becoming proficient with the debugger will help you create robust Java applications.