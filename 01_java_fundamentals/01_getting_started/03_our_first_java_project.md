When starting IntelliJ for the first time you will prompted to change the theme, font size, color accessibility, and keymap. 
You can configure all of these options later, in the Settings menu.
I recommend you to stick to the defaults, expect for maybe switching to the dark theme, if you prefer that (I know I do.)

You don't need to install any plugins, but for the purposes of this course, I will be using the Presentation Assistant plugin,
which shows keyboard shortcuts whenever I use them.

Go ahead and create a new project:
File > New > Project

Name it `java-course`. Place it in the `C:\projects` (Windows) or `~/projects` (Linux) directory. Don't create a Git
repository, unless you know what Git is and how to use it.

Select the following options:
* Language: `Java`
* Build System: `Maven`
* JDK: `openjdk-21` or just about any JDK not older than Java 8
* Add sample code: (leave this unchecked)
* GroupId: `com.bezbos` or your own username. This is merely the root package name of our Java project. It just metadata and it doesn't affect program logic.
* ArtifactId: `java-course` or something else.

After creating the project. IntelliJ will proceed to index the JDK or download the pre-built indexes. If you have decent 
internet speed, I suggest downloading the pre-built indexes that IntelliJ offers. If nothing pops up, IntelliJ will 
manually index the JDK. No biggie, just wait for it to finish.

The first opening of the project is slow because of the initial indexing. Subsequent opening will be much faster.

When the project was created, the basic project structure was generated:
```
📁java-course
├───📁.idea
└───📁src
    ├───📁main
    ├───📁test
    └───📄pom.xml
```

By default, all project that use Maven as the build tool should have a `pom.xml` file which defines project metadata 
and dependencies (among other things.) It should look similar to this:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.bezbos</groupId>
    <artifactId>java-course</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>21</maven.compiler.source>
        <maven.compiler.target>21</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

</project>
```

The `.idea/` directory contains configuration files exclusively used by IntelliJ and it's plugins. You will almost never
have to touch these files.

Inside the `src/` directory is where all of our Java code files and assets will be stored. Inside `src/java/` is where all
our code is going to be stored, while inside `src/resources/` is where assets and configuration will be located.

Inside the `test/` directory is where code files of unit tests are located. This directory also has a `java/` directory for specifically
storing unit tests, but it may also have a `resources/` directory for test assets.

The `External Libraries` list will show you all the project dependencies, including the JDK.

The `Scratches and Consoles` is useful for keeping notes or simply being a placeholder for copy/pasting code and whatnot.

Create a new Java class inside the `src/main/java/` directory. Right-click on `java/` > New > Java Class > ***Application***.

Now we just need to define the entry point of our Java program. Write the following code:
```java
package com.bezbos;

public class Main {
    
    public static void main(String[] args) {
        System.out.println("Hello world!");
    }
    
}
```

IntelliJ is smart enough to recognize the `main` method and on the left side it should offer you to click a play button.
When you click it, select the `Run 'Application.main()'` option.

The program should run and print out the `Hello world!` message in the console.