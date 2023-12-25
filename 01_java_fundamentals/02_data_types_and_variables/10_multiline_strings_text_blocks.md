
Starting with Java 15, you can use multiline strings, sometimes referred to as Text Blocks, or two-dimensional string 
literals. I will refer to them as multiline strings. Multiline strings allow you to define strings in multiple lines 
without having to do concatenation.

Let’s say we have a string that represents an employee experience report:

```java
String employeeExperience = "person:\n"
    + "\tfirstName: Jonh\n"
    + "\tlastName: Doe\n"
    + "\tage: 25\n"
    + "workExperience:\n"
    + "\tEricsson:\n"
    + "\t\tduration: 2 yrs\n"
    + "\tAmazon:\n"
    + "\t\tduration: 1.5 yrs\n";
System.out.println(employeeExperience);
```

It’s very tedious to create this string using concatenation and I had to use escape sequences for indentation. 
With multiline strings you define your desired string without having to do concatenation or escape sequences:

```java
String employeeExperienceMultiline = """
person:
    firstName: Jonh
    lastName: Doe
    age: 25
workExperience:
    Ericsson:
        duration: 2 yrs
    Amazon:
        duration: 1.5 yrs
""";
System.out.println(employeeExperienceMultiline);
```

Now that’s much simpler and it makes our code more readable. All of the indentation has been preserved. IntelliJ will 
mark the beginning of indentation with a green line, so you always know where the indentation begins. If you’re unsure 
of your indentation, try formatting the code by pressing `Control + Alt + L`. This will format the current document and 
it will align the multiline string.

Multiline strings also provide simple, but powerful formatting options. Let’s say we had a database query likes this:

```java
String sql = """
SELECT \
    c."id, \
    c.title, \
    c.description, \
    c.author, \
    c.created_at, \
    c.updated_at \
FROM \
    courses c \
WHERE \
    c.title LIKE "%java%" AND \
    c.created_at BETWEEN '01-01-2022' AND '31-12-2022';
""";
System.out.println(sql);
```

Backslashes `\` are used to provide fake new lines for the sake of readability, but when the string is evaluated, the 
backslashes will remove the line breaks. So we get the benefit of reading the database query as a nicely formatted 
multiline string, but we can send it to the database without excessive line breaks.

We can also very easily apply format specifiers arguments to multiline strings. Let’s take the employee report example 
from the previous lesson, where we used `String.format()` to apply formatting specifiers. We’re going to repeat the example 
with multiline strings:

```java
String firstName = "Jonh";
String lastName = "Doe";
int age = 25;
float averageOvertime = 32.2621F;

String employeeReportMultiline = """
    Employee %s %s is %d years old.
    They have an average overtime of %.1f hours.
    """.formatted(firstName, lastName, age, averageOvertime);
System.out.println(employeeReportMultiline);
```

As you can see we don’t have to call `String.format()` to apply formatting specifiers, instead we simply say formatted 
and pass it the arguments.

Lastly, we can translate escapes in multiline strings which contained escaped escape sequences, like this:

```java
String employeeExperience = """
    person:\\\\n
    \\\\tfirstName: Jonh\\\\n
    \\\\tlastName: Doe\\\\n
    \\\\tage: 25\\\\n
    workExperience:\\\\n
    \\\\tEricsson:\\\\n
    \\\\t\\\\tduration: 2 yrs\\\\n
    \\\\tAmazon:\\\\n
    \\\\t\\\\tduration: 1.5 yrs\\\\n
    """.translateEscapes();
System.out.println(employeeExperience);
```

And we can remove trailing whitespaces:

```java
String sql = """
    SELECT   
        c."id,    
        c.title,   
        c.description,  
        c.author,   
        c.created_at,    
        c.updated_at   
    FROM   
        courses c   
    WHERE    
        c.title LIKE "%java%" AND   
        c.created_at BETWEEN '01-01-2022' AND '31-12-2022';   
    """.stripIndent();
System.out.println(sql);
```

You can show whitespaces in IntelliJ by enabling the “Show Whitespaces” option. Press `Control + Shift + A` to bring up 
the Action menu. Type in “Show Whitespaces” and toggle it by pressing Enter or click on it. You can also change it globally 
by going to _Settings > Editor > Appearance_ and toggle the setting “Show Whitespaces”.

That’s all regarding multiline strings. If you’re using Java 15 or greater, I recommend you make use of multiline strings. 
They will help you write more readable and understandable code.