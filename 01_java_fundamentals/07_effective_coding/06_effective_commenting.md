# Effective Commenting

In programming, commenting is a way of explaining code. Java takes this a step further with JavaDoc comments, allowing
developers to document code with more sophisticated formatting options.

JavaDoc comments provide structured documentation, including information about the purpose, parameters, return values, 
exceptions, and usage examples.

Normal comments should be used to provide context for complex code, but avoid commenting on straightforward code if possible,
as too many comments can be confusing.

When using complex algorithms or data structures, leave links to relevant resources to help other developers understand 
the code.

Use prefixes like `TODO`, `FIXME`, `NOTE`, `WARNING`, and similar prefixes to attract attention to specific parts of the 
code.

When writing comments, keep them concise to convey essential information.

#### Prefer this:

```java
// Calculates the subtotal of the items in the ‘shoppingCart’ array
double subtotal = 0;
for (double item : shoppingCart) {
    subtotal += item;
```

#### Avoid this:

```java
// This is a for-each loop that iterates through the 'shoppingCart' array and calculates the sum of its elements.
// The initial value of the 'subtotal' variable is set to 0, and in each iteration, the current element 'item is added to 
'subtotal'. 
double subtotal = 0;
for (double item : shoppingCart) {
    subtotal += item;
```

While lengthy comments may be correct, they can overwhelm the reader, discouraging them from reading. Concise comments 
provide necessary information without excessive details, making them easy to understand at a glance. 

Writing good comments 
comes with experience. If unsure, consider using a tool like ChatGPT for assistance.