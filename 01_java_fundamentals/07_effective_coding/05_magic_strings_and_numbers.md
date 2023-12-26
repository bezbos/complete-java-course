# Magic Strings & Numbers

**Magic strings** or **magic numbers** refer to the practice of using string and number literals without explaining their 
purpose, or sometimes, flat out repeating the same values in multiple places.

This is a form of code duplication. Changing these magic values requires searching for occurrences in the code, making 
it error-prone to update each place individually.

However, a simple solution exists for magic values. Use variables or constants to represent these values. The variable 
name is self-documenting, usually providing enough understanding. A JavaDoc comment can be added for additional clarification.

For example, when checking if a user has the role admin:
```java
if (user.getRole().equals(ADMIN_ROLE)) {...}
```
Avoid subtle bugs caused by typos or case differences:

```java
if (user.getRole().equals("admin ")) {...}
if (user.getRole().equals("Admin")) {...}
if (user.getRole().equals("administrator")) {...}
```

Solve this issue by extracting the admin role string into a constant:

```java
public static final ADMIN_ROLE = "admin";
```
Now, reuse the constant anywhere you need to check if the user has the admin role. No more worries about typos; if you 
mistype the constant, it results in a compilation error—a straightforward fix.