In this course, we've worked with variables that hold a single value. However, there are cases where we need to 
represent multiple values together. To achieve this, we use arrays.

Arrays are container objects that hold a fixed number of elements of a single type, such as integers, strings, or 
characters. Let's create an array of numbers:

```java
int[] numbers = new int[5];
```
Array data types consist of the element data type and brackets indicating it's an array. The right side uses the `new` 
keyword with the number of elements in brackets.

It's possible to declare arrays in C style, but it's not recommended in Java:

```java
int numbers[] = new int[5]; // C-style declaration, not recommended
```

Now that we've declared an array, we can assign values to it:

```java
numbers[0] = 8;
numbers[1] = 16;
numbers[2] = 32;
numbers[3] = 64;
numbers[4] = 128;
```

When assigning values, specify the index, which starts from 0.

To read elements from an array:

```java
System.out.println("First element: " + numbers[0]);
System.out.println("Last element: " + numbers[4]);
```

You can also declare arrays using a shorter syntax:

```java
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
```

The compiler can infer the array type, so you can omit `new int[]`.

```java
int[] numbers = { 1, 2, 3, 4, 5 };
```

Remember to use plural nouns when naming arrays, reflecting their type, value, and meaning.