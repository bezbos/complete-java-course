If we want to skip an iteration of the loop, without terminating the loop, we can use the `continue` statement. 
Let’s change our previous example up a little, so that it prints out every number, except for the lucky number.

I’m going to reduce the counter limit to 10 so that we can more easily read the output:

```java
int counter = 0;

// we now want a lucky number between 0 and 10
long luckyNumber = Math.round(Math.random() * 10);
while (counter < 10) {

    // check if the counter value equals the lucky number
    if (counter == luckyNumber) {
        // if so, we want to increment the counter and continue to the next iteration
        counter++;
        continue;
    }

    // otherwise we print the counter value and increment the counter 
    System.out.println("Counter -> " + counter);
    counter++;
}
```
Run the program… As we can see, every number except for the lucky number was printed out in the console.

That’s that regarding basic looping. Next, I’m going to show you how to process arrays using loops, and the enhanced for loop which provides the simplest way for processing arrays.