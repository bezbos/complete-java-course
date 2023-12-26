In real-world applications, developers use conditional statements to control the flow of the program, allowing them
to conditionally execute code based on specified conditions.

In Java, the `if` statement is fundamental for controlling the flow of the program. It enables the execution of code 
based on the result of an expression.

```java
int wallet = 800; // represents our balance
int[] itemPrices = {300, 200, 500, 100}; // items available for purchase
int total = itemPrices[0] + itemPrices[3]; // buying the first and last item

if (total > wallet) {
    System.out.println("That's too expensive...");
} else {
    System.out.println("Nice purchase!\t-" + total + " credits");
}
```

The above code checks if the total purchase exceeds the wallet balance and prints a corresponding message.

#### Multiple Conditions
You can use multiple `else..if` statements for different conditions:

```java
else if (total == 0) {
    System.out.println("You didn’t purchase anything.");
} else if (total == wallet) {
    System.out.println("Wow! Your wallet balance matches the total amount!");
}
```

This example adds conditions for when the total is zero or equals the wallet balance.

#### Handling Multiple Conditions
For handling multiple conditions without the `else if` chain, use separate `if` statements:

```java
if (total > wallet) {
    System.out.println("That's too expensive...");
}
if (total == 0) {
    System.out.println("You didn’t purchase anything.");
}
if (total == wallet) {
    System.out.println("Wow! Your wallet balance matches the total amount!");
}
```

Ensure to address the issue of executing the `else` statement:
```java
if (total < wallet) {
    System.out.println("Nice purchase!\t-" + total + " credits");
}
```

This approach allows the execution of both `if` statements independently.

```java
total = 0; // Set total amount to zero
wallet = 0; // Set wallet balance to zero

// Run the program
if (total > wallet) {
    System.out.println("That's too expensive...");
}
if (total == 0) {
    System.out.println("You didn’t purchase anything.");
}
if (total == wallet) {
    System.out.println("Wow! Your wallet balance matches the total amount!");
}
```

Now, both `if` statements get executed based on the specified conditions.