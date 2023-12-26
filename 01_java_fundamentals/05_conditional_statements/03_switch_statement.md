Another mechanism for control flow in Java is the `switch` statement. This statement allows conditional execution of 
code based on a variable value, similar to the `if` statement. However, the `switch` statement is restricted to variables
with certain data types, such as integers, characters, strings, and enums. It is commonly used for checking ranges of values,
while `if` statements are employed for checking expression results.

To illustrate the `switch` statement, let's create a program that accepts a month number as input and displays the 
corresponding month.

```java
// Create a scanner object
Scanner scanner = new Scanner(System.in);

// Prompt the user to enter the month number
System.out.print("Enter month number: ");

// Parse the input to an integer
int monthNumber = Integer.parseInt(scanner.nextLine());
```
Now, let's define the `switch` statement. Declare a variable to hold the month name and specify cases for each month:

```java
String monthName = null;

switch (monthNumber) {
    case 1:
        monthName = "January";
        break;
    case 2:
        monthName = "February";
        break;
    case 3:
        monthName = "March";
        break;
    case 4: 
        monthName = "April";
        break;
    case 5: 
        monthName = "May";
        break;
    case 6: 
        monthName = "June";
        break;
    case 7: 
        monthName = "July";
        break;
    case 8: 
        monthName = "August";
        break;
    case 9: 
        monthName = "September";
        break;
    case 10: 
        monthName = "October";
        break;
    case 11: 
        monthName = "November";
        break;
    case 12: 
        monthName = "December";
        break;
    default:
        monthName = "Unknown month";
        break;
}

System.out.println("Month name: " + monthName);
```
The `default` statement is executed if none of the `case` statements matches. You can also define blocks for `case` statements 
or the `default` statement, but it's often unnecessary due to indentation.

Note that the `break` statement is crucial to exit the switch block; without it, the switch would fall through to subsequent
cases. If you remove `break` statements, all cases would execute.

Keep in mind that `switch` statements are limited to checking variable values and specific data types. Complex conditions 
and non-supported data types require the use of `if` statements.