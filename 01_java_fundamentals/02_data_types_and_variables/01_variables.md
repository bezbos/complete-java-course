Because we're learning the basics of Java in this part of the course, most of our code will
be written in the `main()` method. We'll explore object oriented programming in Java OOP, for now
let's just focus on the fundamental mechanisms of Java.

In Java, we use variables to store values. Each variable has a _name_, _data type_, and a _value_. Variables can be visualized as labeled boxes, with each box corresponding to a name and a specific content type.
```java
int a = 1;
int b = 2;
String c = "Hello";
```

The first part of a variable is its data type, followed by the variable name and the assignment operator. Literal values like `1`, `2`, and `"Hello"` are assigned to the variables. 
Semi-colons `;` denote the _end of statements_ in Java.

Variable names in Java are case-sensitive. For example:

```java
String silver = "Silver";
String SILVER = "Silver";
```

These are two separate variables due to case sensitivity.

Variables can be accessed by writing their exact names:

```java
silver = "Gold";
```

Reassigning values is possible, but exact variable names are crucial due to case sensitivity.

Variables in Java follow the camelCase convention, where each word begins with an uppercase letter:

```java
String silverDescriptionText = "Silver is a precious metal…";
```
Constants use the SCREAMING_CASE notation:

```java
static final int SILVER_ID = 100;
```

Now that we've declared variables, let's perform operations:

```java
int result = a + b;
result = a + result + 10;
```

Here, we added variables and stored results in another variable.

Printing results in the console:

```java
System.out.println("Result: " + result);
```
This method prints content to the console. Use Shift + F9 to build and run the project, or Shift + F10 for a cleaner output without the debugger.

Note: Numbers passed into the `println()` method are implicitly converted into strings, which will be discussed in detail in the section on type casting and conversion.