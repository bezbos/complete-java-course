In this lesson, we explore various operations on arrays in Java.

### Array Length and Access

Arrays in Java have a fixed length, which is immutable after creation. Example:

```java
String[] foo = {"foo", "bar", "baz"};
System.out.println("Length of foo: " + foo.length);
System.out.println("Last element of foo: " + foo[foo.length - 1]);
```
_Note: Array indices start from zero._

### Multidimensional Array Length and Access
You can check the length of nested arrays in multidimensional arrays:

```java
int[][] array2d = new int[2][4];
System.out.println("Parent array length: " + array2d.length);
System.out.println("1st child array length: " + array2d[0].length);
System.out.println("2nd child array length: " + array2d[1].length);
System.out.println("Total element capacity: " + (array2d[0].length + array2d[1].length));
```

### Array Copying
Arrays in Java are reference types, not primitive types. Copying arrays with reassignment doesn't work:

```java
int[] array1 = {1, 2, 3};
int[] array2 = array1; // Copies the handle, not the array
```

To copy arrays, use the `Arrays` utility class:

```java
import java.util.Arrays;
int[] array2 = Arrays.copyOf(array1, array1.length);
```

### Array Printing
Printing arrays directly may not yield desired results. Use `Arrays.toString()` for a readable output:

```java
System.out.println(Arrays.toString(array2));
```

For multidimensional arrays, use `Arrays.deepToString()`.

### Array Sorting and Searching
#### Sorting:

```java
int[] numbers = {8, 32, 1, 4, 2, 16, 64};
Arrays.sort(numbers);
```

#### Searching:

```java
int index = Arrays.binarySearch(numbers, 16);
```

### Array Equality
For content-level equality:

```java
char[] letters1 = {'a', 'b', 'c', 'd'};
char[] letters2 = {'a', 'b', 'c', 'd'};
System.out.println("Are array contents equal: " + Arrays.equals(letters1, letters2));
```

For multidimensional arrays, use `Arrays.deepEquals()`.

### Array Filling
Use `Arrays.fill()` to fill an entire array with a value:

```java
int[] zeroArray = new int[20];
Arrays.fill(zeroArray, 0);
System.out.println(Arrays.toString(zeroArray));
```

These cover basic array operations. Advanced methods are available but are seldom used.