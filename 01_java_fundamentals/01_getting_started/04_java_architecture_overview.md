Java is a programming language that was designed with portability in mind. A common slogan used for Java is 
*“Write once, run anywhere.”*

Programming languages like C++ or Rust are compiled **ahead of time**, meaning that the language is **compiled directly 
to machine instructions** for a specific CPU instruction set architecture.

This approach provides performance benefits, but limits program portability. A C++ or Rust program that is written for 
Windows, will not run on Linux, without being recompiled for Linux. The same issue applies to instruction set architectures. 
A program compiled for x86 CPUs will not run on ARM CPUs.

Java addresses this issue by compiling Java source code into intermediate instructions called **bytecode**. This bytecode 
is then shipped to a **Java Virtual Machine**, which then **compiles the bytecode into machine instructions** for the current system, 
thus providing you with the ability to write once, and run anywhere. The process of compiling bytecode into machine 
instructions is also known as **Just-in-Time compilation** or **JIT** for short

Although this approach does introduce some **performance degradations**, especially on **program startup**, but modern JVMs 
have JIT compilers that **analyze hot-spots** in the code and **additionally optimize these code paths during runtime**. 
There is also the GraalVM Java compiler which pre-compiles and optimizes Java code, and packages it inside a container, 
which allows for much faster startup, lower memory consumption and generally much better performance.

Because the **JVM compiles bytecode to machine instructions**, this means that it’s also possible to have **other languages generate bytecode** 
and have that bytecode get executed on the JVM. Because of this, there already are a few popular **JVM languages** such as 
**Kotlin**, **Groovy** and **Scala**. You could write a program in Kotlin that calls methods from Java, and vice versa.
