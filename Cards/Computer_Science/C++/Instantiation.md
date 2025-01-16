up:: [[C++ MOC]]
tags:: #Programming
# Instantiation
- The creation of an instance or an object of a class

- **Basically doing MyClass::**
##### Examples:

```
class MyClass {
public:
    MyClass() {} // Constructor
};

// Instantiation of MyClass
MyClass myObject; // Automatic allocation
MyClass* myObjectPtr = new MyClass(); // Dynamic allocation

```

## Instantiating functions in main programs:
### 1: Create an instance of a class:
`AmericanOption Test(S, K, r, sigma, b, option_type);`
- Test is the instance here
### Append function to that instance
`Test.Price()`
- Here, we are using the `Price()` function, which calculates a Black-Scholes price, on an instance of AmericanOption
	- In other words, we are calculating the price of an American Option via a `Test` instancr
