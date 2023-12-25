In Java, it's crucial to distinguish between compile-time and runtime processes. The Java compiler manages the compile-time process, while the Java Virtual Machine (JVM) handles the runtime process.

## Compile-Time Process

The compiler translates Java source code into JVM bytecode, checking code correctness and reporting warnings or aborting for errors. Successful compilation results in Java class files containing bytecode.

## Runtime Process

The JVM reads class files, executing bytecode during the runtime. Runtime events include warnings, exceptions, and fatal errors:

- **Warnings:** Reported in the console as logs for unusual situations.
- **Exceptions:** Isolated runtime errors handled by the application.
- **Fatal Errors:** Unrecoverable conditions, like `OutOfMemoryError`, causing program crashes.

### Handling Issues

It's advisable to address as many issues as possible during compilation. Runtime exceptions require analyzing stack traces to identify problems.

## Tiered Compilation

During runtime, the JVM employs tiered compilation. This involves analyzing "hot" code spots and recompiling them with more optimizations. The frequency of code execution determines priority for optimization.

### Historical Context

Tiered compilation was initially introduced as the HotSpot JVM, an iconic name reflecting its functioning.
