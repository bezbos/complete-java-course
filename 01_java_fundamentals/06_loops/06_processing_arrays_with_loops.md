In Java, you can easily process arrays using loops. Loops have a counter variable that can be utilized as the index for 
accessing array elements.

### Using a `while` Loop

```java
// Define an array of window messages
String[] windowMessages = {"resize", "move", "move", "minimize", "restore", "maximize", "exit"};

// Initialize a counter variable
int i = 0;

// Process array elements using a "while" loop
while (i < windowMessages.length) {
    System.out.println("Processing window message \"" + windowMessages[i] + "\"");
    i++; // Increment the counter
}

// Print a message indicating that all messages have been processed
System.out.println("All window messages processed");
```

We’re using the counter variable `i` as the array index. This way, we write the loop one time and process all the 
elements, instead of processing each element individually.

### Using a `for` Loop
```java
// Define an array of window messages
String[] windowMessages = {"resize", "move", "move", "minimize", "restore", "maximize", "exit"};

// Process array elements using a "for" loop
for (int i = 0; i < windowMessages.length; i++) {
    System.out.println("Processing window message \"" + windowMessages[i] + "\"");
}

// Print a message indicating that all messages have been processed
System.out.println("All window messages processed");
```

This is a very effective way of processing arrays. Loops are the foundational concept of every programming language, and
you will be using them extensively in your work, in one form or another.