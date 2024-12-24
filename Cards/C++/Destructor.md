up:: [[Canonical Header File]]
tags:: #Programming
# Destructor
## Purpose
 Used for cleanup operations
	- Releasing recourses, closing files, freeing space, etc...
- [[Virtual Destructor]]
	- Used in [[Inheritance]]
	- When a **base** class uses [[Pointers]] or [[Call by Reference]] to the **derived** class
		- Used in the base class
## Declaration
```
~Point();
```
- Tilda (~) denotes the destructor

## Implementation
```
Point::~Point() {}
```

## With [[Inheritance]]
- The destructor is NOT inherited, instead a [[Virtual Destructor]] is used