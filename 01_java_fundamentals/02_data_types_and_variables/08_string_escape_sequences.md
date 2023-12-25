When working with strings and characters, special characters like a new line, a tab, or a Unicode character need 
representation through escape sequences.

To insert a new line in our string, we would write:
```java
System.out.println("How\nare\nyou\ndoing?");
```

Notice how each word is on a new line. IntelliJ recognizes escape sequences and highlights them.

I’m going to show you Java's escape sequences:

```java
System.out.println("foo\b"); // Delete a single previously typed character
System.out.println("1234\t123\t12\t1\t"); // Insert a tab
System.out.println("page1\fpage2\fpage3"); // Move the text cursor to the start of the next page. Since our console is not a printer, we’ll get an unknown character symbol.
System.out.println("now you see me\rnow you don’t"); // Return the cursor to the beginning of the current line, undoing anything before it in that line.
System.out.println("\"Some quote\""); // Insert a double quote, useful when using double quotes in strings.
System.out.println('\''); // Insert a single quote, useful when declaring character variables
System.out.println("\\ a comment"); // Insert a backslash, useful when escaping the backslash itself.
```

You can also use UTF-16 characters, escaping them with a Unicode escape sequence. For example, printing `Hello! How are you doing?` in Swedish:

```java
System.out.println("Hall\u00e5! Hur m\u00e5r du?");
```

Use any Unicode character by typing `\u` and the hexadecimal code of that character.