Since Java 5, there is an additional form of the `for` loop, called the _enhanced for_ loop which can only be used with 
arrays and collections.

With the enhanced for loop you don’t have to specify the test condition or iterate a counter variable, instead you only 
tell it what array or collection you want to iterate over. 

Here is an example:
```java
String[] windowMessages = {"resize", "move", "move", "minimize", "restore", "maximize", "exit"};

// here we’re basically saying, for each message in windowMessages, do this
for (String message : windowMessages) {
    System.out.println("Processing window message \"" + message + "\"");
}

System.out.println("All window messages processed");
```

As we can see, that is cleaner and more readable than a conventional `for` loop. This is the loop you will be using the
 most in Java because whenever you need to iterate over a collection, this is the cleanest and most readable way of doing
  so. 

At some point, you are going to learn about Collections and Streams which are much more powerful for processing data, 
  but keep in mind that they all use loops under the hood.