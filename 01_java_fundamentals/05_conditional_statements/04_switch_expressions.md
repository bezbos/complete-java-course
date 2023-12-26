Since Java 14, a new control flow mechanism has been introduced into the language. It’s called the switch expression, 
a more flexible and cleaner alternative to switch statements. As a switch "expression," it can be chained to other 
expressions, like assignment or arithmetic expressions.

Let’s rewrite the previous switch statement as a switch expression:

```java
String monthName = switch (monthNumber) {
    case 1 -> "January";
    case 2 -> "February";
    case 3 -> "March";
    case 4 -> "April";
    case 5 -> "May";
    case 6 -> "June";
    case 7 -> "July";
    case 8 -> "August";
    case 9 -> "September";
    case 10 -> "October";
    case 11 -> "November";
    case 12 -> "December";
    default -> "Unknown";
};
```

Here, "arrow case labels" `->` indicate the value returned for the matching case. We don’t need `break` statements, 
making the code cleaner and more readable.

If you want to return the same value for multiple cases, specify multiple values in the `case` declaration:

```java
case 1, 2, 3, 4 -> "January-April";
case 5, 6, 7, 8 -> "May-August";
case 9, 10, 11, 12 -> "September-December";
```

Because switch expressions are "expressions," you can combine them with other expressions:

```java
String monthName = switch (monthNumber) {
    // ...
} + " is the name of the " + monthNumber + " month.";
System.out.println(monthName);
```

You can even pass the entire switch expression to a `println()` method:

```java
System.out.println(switch (monthNumber) {
    case 1, 2, 3, 4 -> "January-April";
    case 5, 6, 7, 8 -> "May-August";
    case 9, 10, 11, 12 -> "September-December";
    default -> "Unknown";
});
```

Switch expressions can include blocks. Since each case of the switch expression returns a value, use the keyword `yield`:

```java
String monthName = switch (monthNumber) {
    case 1 -> {
        System.out.println("You entered January");
        yield "January";
    }
    // ...
};
```

Remember, if you don’t define the `yield` statement, you will get a compilation error.

In conclusion, switch expressions can be used to conditionally get a value, depending on a variable value. They are 
generally better than switch statements because they are cleaner to write and more flexible in their application.