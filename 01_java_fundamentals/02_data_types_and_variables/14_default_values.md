Primitive types in Java have default values and are assigned only to static variables and class member variables. Variables declared inside methods without assignment cannot be accessed:

```java
public static void main(String[] args) {
    int a;
    System.out.println(a); // this will not compile
}
```

However, static or class member variables have default values and can be accessed:

```java
public class Application {
    static double PI;
    double pi;
    
    public static void main(String[] args) {
        System.out.println(PI);
        // System.out.println(pi); // this would work inside a non-static method
    }
}
``` 
Press `Shift + F10` to run the project, and it prints out zero.

The `static` modifier makes variables belong directly to the class, while non-static variables are called "_member variables_." 
Variables declared inside methods are "_local variables_," and those outside methods within the class block are "_member variables_" 
or "_fields_." If they have the `static` modifier, they are called "_static variables_" or "_class variables_." 
`static final` variables are _constants_.

This might be confusing now, but it will become clearer in the second part of the course, "Java OOP."

Let's examine default values of all types:
```java
public class Application {
    static byte defaultByte;
    static short defaultShort;
    static int defaultInt;
    static long defaultLong;
    static float defaultFloat;
    static double defaultDouble;
    static char defaultCharacter;
    static boolean defaultBoolean;
    static String defaultString;

    public static void main(String[] args) {
        System.out.println("Default Byte = " + defaultByte);
        System.out.println("Default Short = " + defaultShort);
        System.out.println("Default Int = " + defaultInt);
        System.out.println("Default Long = " + defaultLong);
        System.out.println("Default Float = " + defaultFloat);
        System.out.println("Default Double = " + defaultDouble);
        System.out.println("Default Character = " + defaultCharacter);
        System.out.println("Default Boolean = " + defaultBoolean);
        System.out.println("Default String = " + defaultString);
    }
}
```

Strings are technically not a primitive type but a reference type. The default value for all reference types is `null`, 
signifying the absence of an object handle.