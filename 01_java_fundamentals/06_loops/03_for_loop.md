The most popular loop type in all programming languages is the `for` loop. It groups all the loop components in its 
signature, making it practical and easy to understand at a glance.

Let's use the example of processing fictional messages with a `for` loop:

```java
int numOfMessages = 5;
for (int i = 0; i < numOfMessages; i++) {
    System.out.println("Processing message " + i);
}
```

We could replace `i < numOfMessages` with `i < 5`, but for illustration, we're assuming `numOfMessages` was received as 
an outside parameter.

#### Step-by-step breakdown
The `for` loop contains three expressions inside the parentheses:
1. The initialization expression (counter variable).
2. The termination expression (test condition).
3. The increment expression.

This time, messages are processed from bottom to top as we started incrementing from 0 to 5. To process from top to bottom,
reverse the loop logic:

```java
int numOfMessages = 5;
for (int i = numOfMessages; i > 0; i--) {
    System.out.println("Processing message " + i);
}
```

#### Omitting expressions
You can omit expressions in the parentheses. For example, omitting the counter variable declaration:

```java
int numOfMessages = 5;
for (; numOfMessages > 0; numOfMessages--) {
    System.out.println("Processing message " + numOfMessages);
}
```

Or placing the decrement expression inside the loop body:

```java
int numOfMessages = 5;
for (; numOfMessages > 0;) {
    System.out.println("Processing message " + numOfMessages--);
}
```

#### Creating an infinite loop:

```java
for (;;) {
    System.out.println("Processing message " + numOfMessages--);
}
```

Infinite loops run forever. In Java, creating intentional infinite loops is rare. If you need continuous execution, 
ensure your loop checks a boolean variable like `boolean isGameRunning` to have a way to terminate it.

In terms of popularity, the `for` loop is the most popular, followed by the `while` loop, and then the `do..while` loop.