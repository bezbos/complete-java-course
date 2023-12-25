Formatting strings with many parameters can be tedious because you have to concatenate many strings and parameters together.
Let’s say we have to print out a report for an employee:
```java
String firstName = "Jonh";
String lastName = "Doe";
int age = 25;
float averageOvertime = 32.2621F;
String employeeReport =
    "Employee " + firstName + " " + lastName + " is "
    + age + " years old and has average overtime of "
    + averageOvertime + " hours.";
System.out.println(employeeReport);
```

As we can see this code is quite messy, but we can make it better by using string formatting:
```java
String employeeReportFormatted = String.format("Employee %s %s is %d years old and has average overtime of %.1f hours.",
                  firstName, lastName, age, averageOvertime);
```

Each format specifier starts with the _percent sign_ `%` and ends with what’s called a _conversion_. Each specifier sequentially 
corresponds to the provided arguments. The percent sign is merely used as an indicator for the formatter that this is a 
specifier. The conversion indicates how the argument is supposed to be interpreted. Before the conversion, we can also 
specify additional parameters like precision, width, flag, and argument index.

I’m going to go through some examples, but you don’t have to remember these and you can always come back here and use 
this material as a reference. We can use `System.out.printf()` or `System.out.format()` to apply format specifiers to strings 
without having to call `String.format()` before that. Both of these methods behave exactly the same:
```java
System.out.printf("%.2f%n", 1.123456); 
// this will print out only the first two decimal places

System.out.printf("X: %4s\nY: %4s\n", 128, 32);
// this will print out numbers and strings with a
// minimum width of 4 characters and will fill
// with spaces if necessary

System.out.printf("X: %04d\nY: %04d\n", 128, 32);
// this will print out numbers with a minimum width of
// 4 digits and will fill with leading zeroes if necessary

System.out.printf("X: %+4d\nY: %+4d\n", 128, 32);
// this will print out numbers with their sign

System.out.printf("No invisible sign padding\nX: %d\nY: %d\n", -128, 256);
System.out.printf("Invisible sign padding\nX: % d\nY: % d\n", -128, 256);
// this will help numbers align by adding a space
// to if the sign is not visible

System.out.printf("X: %(d\nY: %(d\n", 128, -32);
// this will surround negative values with parenthesis
// we can use spaces in front of parenthesis to help
// align the numbers

System.out.printf("X: % (d\nY: % (d\n", 128, -32);
System.out.printf("X: %-4d\nY: %-4d\n", 128, 32);
// this will align numbers to the left and add spaces
// on the right side
```

For this example, I’m going to change locales. In Java locales are used to define how certain numbers and strings should 
be formatted, like date and time, currency and so on. In this case changing the locale will change the decimal separator:

```java
Locale.setDefault(Locale.GERMAN);
System.out.printf("Germany separators & delimiters: %,f\n", 100_000_000.000000);
Locale.setDefault(Locale.US);
System.out.printf("US separators & delimiters: %,f\n", 100_000_000.000000);
```
So as we can see, depending on the currently selected locale, a different thousand separator and decimal separator will 
be used. You can also pass the locale directly to `System.out.printf()` like this. You can do the same with `String.format()`.

We can use argument index parameters to specify which argument should be used for a given specifier:

```java
System.out.printf("%3$d %2$d %1$d\n", 10, 20, 30);
```

So now we've printed out the arguments in reverse order. We can also specify that we want the argument of the previous specifier:

```java
System.out.printf("%6$d %<d %4$d %<d %2$d %<d\n", 10, 20, 30, 40, 50, 60);
```

So this will take the 6th argument, then on the next specifier, it will take the previous specifier's argument, which 
was the 6th argument, and so on...

Formatting specifiers are quite comprehensive and I’ve explained the fundamentals. If you wish to learn more about them, 
you can easily find explanations and samples online.