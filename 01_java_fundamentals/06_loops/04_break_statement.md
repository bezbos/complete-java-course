Loops in Java have termination conditions, but sometimes we need to exit the loop earlier. To achieve 
this, we can use the `break` statement.

The `break` statement, familiar from switches, exits the loop when used inside it. For example:

```java
// Declare a counter variable starting at zero
int counter = 0;

// Pseudo-randomly generate a lucky number not exceeding 100
long luckyNumber = Math.round(Math.random() * 100);

// Use a "while" loop with a maximum of 100 iterations
while (counter < 100) {
    // Check if the counter value matches the luckyNumber
    if (counter == luckyNumber) {
        // Break out of the loop
        break;
    }
    // Increment the counter otherwise
    counter++;
}

// Print out the lucky number
System.out.println("Finished at number " + counter);
```

Running the program shows that the loop terminates as soon as it reaches the lucky number. Multiple runs yield different 
lucky numbers. This demonstrates how to use the `break` statement to specify additional termination conditions inside the 
loop body.