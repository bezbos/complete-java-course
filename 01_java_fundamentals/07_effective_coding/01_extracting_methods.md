In real-world Java projects, breaking down complex business logic into smaller, manageable pieces is essential for code
readability, maintenance, and reuse. Methods play a crucial role in achieving this organization.

Consider a program calculating the total cost of an order. While functional, the code lacks reusability. Extracting logic
into methods enhances maintainability and reduces error-prone code.

```java
double[] items = {29.99, 14.99, 12.49, 11.19};
double weight = 5;

double subtotal = calculateSubtotal(items);
double discount = calculateDiscount(subtotal, 15);
double tax = calculateTax(subtotal, 25);
double shippingFee = calculateShipping(subtotal, weight);
double total = (subtotal - discount) + tax + shippingFee;

System.out.println("Your total is " + total);
```

### Extracting Methods
Refactoring the code involves creating methods for specific calculations:

```java
public static double calculateSubtotal(double[] items) {
    double subtotal = 0;
    for (double item : items) {
        subtotal += item;
    }
    return subtotal;
}

public static double calculateDiscount(double amount, double discountPercentage) {
    return amount * (discountPercentage / 100);
}

public static double calculateTax(double amount, double taxPercentage) {
    double tax = (amount > 100) ? amount * (taxPercentage / 100) + 2 : amount * (taxPercentage / 100);
    return tax;
}

public static double calculateShipping(double amount, double weight) {
    double shippingFee = (weight > 5) ? amount * (7.0 / 100) : amount * (5.0 / 100);
    return shippingFee;
}
```
Now, the `main()` method is concise and easy to understand:

```java
double subtotal = calculateSubtotal(items);
double discount = calculateDiscount(subtotal, 15);
double tax = calculateTax(subtotal, 25);
double shippingFee = calculateShipping(subtotal, weight);
double total = (subtotal - discount) + tax + shippingFee;
```

This approach enhances code maintainability and readability while promoting reusability.