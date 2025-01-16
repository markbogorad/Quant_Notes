up:: [[STL Implementation]]
tags:: #Programming
# Templates
- Allows for **reusable** code by allowing for multiple data types in the same code (template)
	- Code behaves the same way for all data types
- When you use a template, you specify the specific types to use via **template parameters**
	- Ex: `template <typename  T, int N>` 
	- While a typename parameter encompasses multiple data types, additional parameters can come in to interact with typename throughout the implementation
		- ![[Screenshot 2024-04-21 at 9.58.58 AM.png]]
			- Size_t is a unique data type in C++ and Size is the generic name for it
## How they work
- Compiler generates code at compile time based on the types with which the templates are instantiated. 
	- Class can store multiple other classes with easier maintenance when compared to generic OOP
- Allows for **type safety** and efficiency, as the operations are tailored for the specific types used.
## Function Templates
- Allows for a blueprint of a function that can be operate on any data type:
- Example:
	- ![[Screenshot 2024-04-21 at 10.04.11 AM.png]]
	- Max can now operate on any T data type
	- Max uses the ternary operator to return X if its greater than Y, otherwise return Y (return the greater of the two)
- In main:
	- ![[Screenshot 2024-04-21 at 10.05.34 AM.png]]
		- Line 1 is int, line 2 is double, line 3 is char
			- Compiler uses T as a placeholder for all of these individually

## Class Templates
- Templates that define entire classes that can operate on any type
```
template <typename T>
class Box {
public:
    Box(T value) : contents(value) {}
    T getContents() { return contents; }
private:
    T contents;
};


// Testing

// Int instantation
Box<int> intBox(123); 
// String instantation
Box<std::string> stringBox("Hello, World!"); 
```
## Template Implementation Key Moments:
### Usage of Parameters (T)
- Templates use parameters in implementation (like T in template typename T) as essentially placeholders for the data type that will be provided on institution
- In templates, just **stick to the template name as the data type**
	- Ex: double value --> T value
#### Non-Type Parameters
- Inserting a datatype instead of a typename into the template
- Used for passing values as parameters
	- In practice example: array size (int size_t)
#### Constraints:
- Things get weird when trying to do **operations** on variables of 2 of the same typenames (2 typename T variables)
	- Operations need to be incorporated in the template for this
### Key about templates:
- References are now to the template instead of object
	- Ex: T instead of Point
- Class now has template attached when referenced
	- Ex: Array becomes Array$<T>$
- All implementations must be part of template
	- Ex: declared as Array$<T>$
- Implementations should be **as generic as possible** and have **minimal functionality** to leave it open to different kinds of implementation and testing 
	- For additional functionality, better to make a **derived class** under the same template 
- ![[Screenshot 2024-03-29 at 7.26.50 PM.png]]
## Naming Templates
- Pick a good name to not get confused
	- class name + type
		- Ex: ShapeT