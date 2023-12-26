
The final step in developing a Java application is building and packaging. This involves compiling the source code, collecting
necessary dependencies, and packaging everything into a distributable format that can be easily executed by end-users or
deployed on a server.

At the core of every Java application are `.java` files, which contain the source code. They are effectively just text files,
but their `.java` extension serves as a flag for code editors to indicate that the contents of these files should be interpreted 
as Java code.

The Java source code must then be compiled into JVM bytecode. This is done by invoking the Java compiler tool `javac`. The
compiler is usually invoked by build tools like Maven or Gradle, and they also handle collecting and including all necessary 
dependencies.

In this course, I’m teaching you the core Java language and how to use built-in methods and classes. An average command-line 
Java application doesn’t really need any dependencies, but there are some very useful ones that you will be adding to almost
any Java project simply because they will make your life easier.

When we instantiated this Java project, we picked Maven to be our build system, so I will show you how to add a dependency 
to a Maven project. Other build systems such as Gradle or Ant have a nearly identical way of adding dependencies, so if you 
learn to add dependencies to Maven, you will know how to add dependencies to Gradle or Ant.

I will also show you how to manually add dependencies, compile, and run a Java project. You’re highly unlikely to ever have
to do this, but it’s good to know because that’s exactly what build tools do under the hood.

### Adding Dependency to Maven Project

To add a dependency to a Maven project, open the `pom.xml` file defined in the root directory of your project. This is an 
XML formatted file and may contain various configurations for building your Java project.

Add a dependencies tag:

```xml
<dependencies>
    <!-- Add dependencies here -->
</dependencies>
```
Now we can add a dependency. I will be adding a very popular library for string manipulation, Apache Commons Lang, which 
contains very useful methods for solving common string manipulation problems. First, we need to find this library in one 
of the public Maven repositories, usually being https://mvnrepository.com. Open it up. Pick the latest version, which at the time 
of this recording is `3.14`.

Copy the XML from the text box and paste it into the `pom.xml` dependencies section:
```xml
<dependencies>
    <!-- https://mvnrepository.com/artifact/org.apache.commons/commons-lang3 -->
    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-lang3</artifactId>
        <version>3.14.0</version>
    </dependency>
</dependencies>
```

IntelliJ and most popular IDEs are smart 
enough to detect changes in this file and immediately offer you to refresh Maven, which will download the dependency.

If for some reason this option doesn’t appear for you, you can open the Maven sidebar and click the **Reload All Maven Projects**
button.

This will instruct Maven to process any changes; in this case, a new dependency will be downloaded and added to the project.

### Using Apache Commons Lang
Once that is done, we can start using the Apache Commons Lang classes and methods. Go back to the `Application` class. Let’s
call some methods that come with Apache Commons Lang.

```java
String a = StringUtils.capitalize("hello world");
System.out.println("a: " + a);

Double b = NumberUtils.createDouble("1.24");
System.out.println("b: " + b);

Double c = NumberUtils.createDouble(null);
System.out.println("c: " + c);
```

This method will capitalize the provided string. It’s very practical and saves us time.

This method will attempt to convert a string into a number using the `Double.valueOf()` method. However, before attempting 
conversion, it will check if the provided string is `null`. If it is, it simply returns `null`, preventing an exception from 
being thrown by the `valueOf()` method.

### Manual Build and Run
Now, in this example, Maven has triggered the building, packaging, collected dependencies, and started our Java application
 for us. That is how you will be building and running Java applications most of the time, but let me show you how it’s done 
 manually. This way you will understand a part of what Maven does in the background when we invoke it.

First, we need to compile the Java source code into JVM bytecode. To do that, we need to have a Java Development Kit (JDK) installed
 on our system. We’ve already done that. Now we need to open up a terminal and navigate to our project’s directory where the 
 entry point class is located.

Open your terminal or command-line if you’re on Windows. Change into the project directory where the `Application.java` file 
is located:

```bash
# Linux
cd ~/projects/java-course/src/main/java

# Windows
cd C:\projects\java-course\src\main\java
```

Now we need to invoke the Java compiler to generate JVM bytecode:

```bash
# Linux
javac -classpath /home/username/.m2/repository/org/apache/commons/commons-lang3/3.14.0/commons-lang3-3.14.0.jar Application.class

# Windows
javac -classpath C:\Users\username\.m2\repository\org\apache\commons\commons-lang3\3.14.0\commons-lang3-3.14.0.jar Application.class
```

If we list the directory files, notice there is a new file `Application.class`. This file contains the JVM bytecode. Now we need 
to run that bytecode:

```bash
#Linux
java -classpath /home/bosko/.m2/repository/org/apache/commons/commons-lang3/3.14.0/commons-lang3-3.14.0.jar:. Application

#Linux
java -classpath C:\Users\username\.m2\repository\org\apache\commons\commons-lang3\3.14.0\commons-lang3-3.14.0.jar:. Application
```

And we get identical output to what we would get if we ran the project through IntelliJ, with the exception of a few flags
 that may be set by IntelliJ or Maven. As I’ve mentioned before, you’re unlikely to ever have to run these commands manually, 
 but I wanted to show you how it’s done, just in case you ever need to create your own build script or use an existing one.