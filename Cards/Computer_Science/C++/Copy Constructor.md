up:: [[Canonical Header File]]
tags:: #Programming
# Copy Constructor
## Purpose:
- Ensure complete duplication of an object maintaining independence between the original object and the copies
- Used when and object needs to be initialized with the state of another object of the same class
	- EX: 
		Point obj1;
		Point obj1=obj2; // Copy constructor used
- Used when **Passing by Value**
	- EX:
		void print_point(Point pt);
			- Copy of the argument is made to pass onto the function
- Used when ending a program (return 0)

### Steps:
1. Initialize one object from another
2. Ensure deep copying

## Declaration
```
	MyClass(const MyClass& other);
```
- Const: Ensures original object is copied and not modified
- MyClass& other: Reference to an instance (other) of the same class (point). The new object will copy onto "other".
- Step 1: Here, you are initializing one object (other) from another (MyClass)

## Implementation
```
	MyClass::MyClass(const MyClass& other) : member(other.member) {}
```
- #### member(other.member)
	- member --> a *member variable* of the object is constructed. A *member variable* is just a variable defined within a class
	- ##### other.member
		- other --> name of the source object onto which the data will be copied
			- An arbitrary name for copies
		- .member --> accesses the specific member variable of the *other* object
	- This expression **accesses** the value of the *member variable* from the *other object*
		- Like saying "copy **member** into *other* **member** object"
- ##### General copy constructor implementation syntax is similar
	- tile(other.title)
	- pages(other.pages)

## With [[Inheritance]]
```
	MyClass::MyClass(const MyClass& other) : BaseClass(), member(other.member) {}
```
- Just declare the base class right after the colon




