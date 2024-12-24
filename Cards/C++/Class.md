up:: [[C++ MOC]]
tags:: #Programming
# Class Declaration
```
class Point {
private:
	 // Internal integers
public:
	// Constructors 
	// Destructor
	// Functions
	// Operators
}
```

## Private Members

- These are variables that represent the internal state of the object
	- Ex: bank account
		- Need this for functions (public), but don't want the account info to be public (keep private). 
- External access to these variables should not be needed
- If a private variable needs to trigger a specific behavior, need to provide public implementation methods (parameterized constructor & etc)
- Can give access with [[Friend]] keyword
###### EX:
```
class Point {
private:
 double x
 double y // coordiantes of the point
 };
```
## Public Members
- [[Canonical Header File]]
- [[Functions]]
- [[Operators]]


