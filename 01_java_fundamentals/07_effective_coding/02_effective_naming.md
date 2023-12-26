
## Variable Names
In order for our code to be readable and maintainable, we need to learn to properly name our variables, methods, classes,
and other constructs. Let’s start with naming variables. Variable names should as clearly as possible describe the purpose
and the content of the variable, and the name shouldn’t be too long if you can help it.

Here are examples of how Java variables should be named:

```java
String personName;
double totalAmount;
int screenWidth;
boolean isLocked;
boolean hasAccess;
boolean canChangeStatus;
int[] luckyNumbers;
List<String> favoriteGenres;
static final String ROLE_ADMIN;
static final List<String> ROLES;
```

The variable names clearly represent their contents. They are short, descriptive, and meaningful. Variable names in Java 
are written in camel-case notation, but constants are written in screaming-case notation. Variable names should use singular 
nouns unless they represent an array or a collection, in which case we use plural nouns. Variables representing boolean values
should begin with prefixes "is", "has", "can", and similar ones.

### Long Variable Names

In practice, you won’t always be able to avoid long variable names, but there are naming strategies you can use to clarify 
long names. For example, say we’re working on an application for land and cadastre operations. Somewhere in the codebase, we 
have a variable that represents a map of cadastral parcel identifications which are grouped by main book ID and land registry
unit ID. The name of such a variable would look like this:

```java
Map<String, List<CadastralParcelIdentification>> cadastralParcelIdentificationsByMainBookIdAndLrUnitId;
```

As we can see, it’s quite verbose. We can make long variable names readable by using underscores, like this:

```java
Map<String, List<CadastralParcelIdentification>> cadastralParcelIdentifications_By_MainBookIdAndLrUnitId;
```

Notice how immediately it becomes easier to read the variable name. That’s because underscores separate the name into 
logical parts. The first part of the name "cadastralParcelIdentifications" tells us that this is a collection. The next part
"By" tells us that the elements of this collection are grouped by something. The last part tells us they’re grouped by the 
composite value of main book ID and land registry unit ID.

### Bad Variable Names

#### Use camel-case notation
We should use camel-case notation for naming variables, unless we’re dealing with excessively long names, in which case 
it’s acceptable to use underscores to logically organize parts of the name:
```java
String PersonName;
int personage;
String person_address;
```

#### Avoid confusing names
Avoid single-character names, cryptic names or abbreviations, unless they really make sense:
```java
String pName;
int pAge;
int cadMunIdentifications; 
```
#### Avoid lengthy names
Avoid overly descriptive or lengthy names:
```java
String nameOfThePerson;
int ageOfThePerson;
```

#### Use plural nouns for arrays and collections
Use plural nouns for array and collection type variables to indicate that they represent multiples of something:
```java
Person[] person;
List<String> genre;
```

#### Use boolean prefixes
For boolean variable names, use prefixes "is", "has", "can" or similar ones:
```java
boolean locked;
boolean accessible;
boolean statusChangeable;
```

#### Struggling to come up with names?
If you’re struggling to come up with a good variable name, check how similar variables have been named, or try using a 
tool like ChatGPT to help you come up with a good name.

#### Naming constants
Constants in Java are static variables, aka class variables with the `final` modifier. These variables can only be assigned 
once and cannot be reassigned thereafter. Constants should always be named using screaming-case notation:
```java
static final int DRAFT_PREPARATION = 1;
static final int EVALUATION_PENDING = 3;
static final int READY_FOR_PUBLISHING = 5;
```

## Method Names
Methods should also follow similar naming practices, where the names should describe the action or behavior they’re 
representing:

##### Good method naming
```java
double calculateSubtotal();
String truncateString();
Expression evaluateExpression();
```

##### Bad method naming
```java
double calcSub();
String truncStr();
Expression evalExpr();
```

#### Using abbreviations
Unnecessary abbreviations should be avoided. It’s alright to use abbreviations to shorten excessively long variable names,
or abbreviations which are commonly used in your project. There are also universally recognized abbreviations like "ID", 
"UUID", "XML", "HTML", and so on, and it’s fine to use these.

```java
long getId();
UUID generateUuid();
XmlDocument readXml();
HtmlDocument parseHtml();
boolean exportPdf();
LrParcel getLrParcel(); // Land registry parcel
CadParcel getCadParcel(); // Cadastral parcel
```

But do not unnecessarily create abbreviations for names like `calculateTotal`. The name is short and simple and doesn't 
need any abbreviating.

#### Use camel-case notation
Methods should also be named using camel-case notation, like variables:

##### Good method naming
```java
double calculateSubtotal();
```

##### Bad method naming
```java
Double CalculateSubtotal();
```

### Method Name Categories
All the rules used for naming variables can be applied to naming methods; however, since methods represent actions and 
behavior, we could categorize their names by their actions.

Let’s see some commonly used method names in Java. 

#### Retrieval Methods
We have retrieval methods that usually retrieve one or more values:

```java
getName(); // Retrieves a person’s name
getFirstOrDefault(Object defaultValue); // Retrieves the first element of a collection or a supplied default value
getGenres(); // Retrieves a byte array, representing the current string
```

#### Error Handling Methods
Error handling methods will usually attempt an operation but will throw an exception upon failure:

```java
getFirstOrThow(); // Retrieve the first element of a collection, if no element exists it will throw an exception
orElseThrow(); // Retrieve a value if present, otherwise throw an exception
```

#### Validation Methods
Validation methods usually check if one or more conditions are satisfied, and if they’re not, they throw an exception or
perform some other operation:

```java
requireNonNull(Object value); // Checks if the parameter is null, if so, throws an exception
requireNonNullOrElse(Object value, Object defaultValue); // Checks if the parameter is null, if so returns the default value
requireInRange(double value, double min, double max); // Checks if the value is not less than min and greater than max
```

#### Conversion Methods
Conversion methods usually convert from one type into another:

```java
toDouble(); // Converts a number into a double
parseInt(); // Converts a string into an integer
```

#### Predicate Methods
Predicate methods usually return a boolean indicating if something is true or false:

```java
isEven(); // Checks if the number is even
hasChildren(); // Checks if a parent node has child nodes
isConnectionAlive(); // Checks if the database connection is alive
```
#### Authorization Methods
Permission or authorization methods are basically predicate methods with a focus on checking if a user or object has 
permissions to do something:

```java
canAccessResource(); // Checks if the account can access a certain resource
hasRole(String role); // Checks if the account has a specific role
canChangeStatus(); // Checks if the user can change some status
```

#### Action Methods
Action methods are methods that perform a specific action or operation:

```java
saveChanges(); // Saves some changes to the database
performCleanup(); // Performs some sort of resource cleanup
sanitizePath(); // Removes illegal characters from a directory path
```

#### Initialization Methods
Initialization methods are methods that usually initialize an object’s state and they usually begin with "init" or 
"initialize":

```java
initialize(); // Initializes the object
initializeBean(); // Initializes the Java bean
```

#### Hook or Lifecycle Methods
Hook or lifecycle methods are methods usually invoked by another component of the system when a certain event occurs:

```java
onValueChanged(); // Executes when the value of something has changed
onSuccess(); // Executes when an operation completed successfully
beforeCommit(); // Executes before a change has been committed
afterCommit(); // Executes after a change has been committed
```

We could spend all day going over various method names and their categories, but the list is endless and is always expanding. 
I wanted to show you some commonly used method names as a reference point.

## Package Names
Java package names should always be in lowercase and should represent a real or fictional internet domain name, but in 
reverse:

```java
com.google.maps.layers
com.bezbos.validation.utils
com.ericsson.network.io
```

## Class Names
Classes are something we will not dive into class details because I have a second part of the course dedicated to Java 
classes and other OOP concepts, but it won’t hurt to explain how they’re named.

When naming classes, we should use nouns to better represent real-life objects. For example:
```java
class Person {}
class Role {}
class Vehicle {}
```

Avoid class names that imply actions:
```java
class Speak {}
class Drive {}
class Perform {}
```

Class names should be in capitalized camel-case notation.

Avoid this when naming classes:
```java
class person {}
class role {}
class vehicle {}
```