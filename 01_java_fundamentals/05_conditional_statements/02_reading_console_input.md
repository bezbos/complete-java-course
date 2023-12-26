In Java, you can read input from the console to build interactive programs where user input plays a role. Using `if`
statements allows you to conditionally execute code based on this input.

For instance, let's ask the user to enter their age:

```java
System.out.print("Enter your age: ");
int age = Integer.parseInt(scanner.nextLine());
```

Here, we use a `Scanner` object to read input from the console. `System.in` represents the console input stream.

Now, let's conditionally print messages based on the entered age:

```java
if (age > 18)
    System.out.println("You are an adult");
else if (age > 14 && age < 18)
    System.out.println("You are a teenager");
else if (age > 4 && age < 14)
    System.out.println("You are a child");
else if (age > 1 && age < 4)
    System.out.println("You are a toddler");
else
    System.out.println("You are a baby");
```
Feel free to adjust the code for your preferences. While omitting braces for one-line statements is possible, many Java 
developers prefer using braces for better clarity and consistency.