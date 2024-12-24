up:: [[Canonical Header File]]
tags:: #Programming
# Parameterized Constructor
## Purpose:
- Accepts variables
- Sets up private variable implementation
- Allows for object initialization at **specific** values 
	- Used to initialize objects with custom values (not default)
- Used when:
	- Want to create an object of the same class but for a different, unique purpose and *give it a different state*
	- Overloading constructors: have multiple parameterized constructors with different parameters
## Declaration
```
MyClass(int initA, int initB);
	int a;
	int b;
```

## Implementation
```
MyClass::MyClass(int initA, int initB) : a(initA), b(initB) {}
```

- The values of integers A and B are initialized to initA (initializer A) and initB. InitA and initB are then utilized within a [[Test Program]] and can be altered there
- Integer A will take value of whatever "initA" will be in the main test program (same for B)

## With [[Inheritance]]
```
MyClass::MyClass(int initA, int initB) : BaseClass(), a(initA), b(initB) {}
```
- Just declare the base class right after the colon
