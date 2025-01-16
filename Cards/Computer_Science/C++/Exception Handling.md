up:: [[C++ MOC]]
tags:: #Programming 
# Exception Handling
## Purpose
- Used to managed runtime errors within a program
### Exception
- an exception is essentially an error: an event or condition that alters the flow of execution of the program
### How they are handled
- #### Try Block
	- A try block is used to wrap code that might generate an exception. It's followed by one or more catch blocks.
- #### Catch Block
	- A catch block contains code to handle the exception. 
	- It specifies the type of exception it can handle. 
	- When an exception is thrown, the catch block that matches the exception type is executed.
- #### Throw Statement
	- The throw statement is used to generate an exception. 
	- It can throw any object as an exception, but it's common to throw objects of classes derived from the standard `std::exception` class.
### Example:
```
try {
    // Code that might throw an exception
    if (errorDetected) {
        throw std::runtime_error("An error occurred");
    }
}
catch (const std::runtime_error& e) {
    // Handle the exception
    std::cerr << "Caught an exception: " << e.what() << std::endl;
}
```
- errorDetected is true
- Exception: runtime_error is thrown
- Catch block matches run_time error exception and catches it
- Catching by reference:
	- const std::runtime_error& e
		- Reference to runtime_error via e variable (e=exception)
	- e.what 
		- What
			- this is a string about the type of exception thrown
				- Think of this as just part of displaying the error message
		- e
			- Represents *exception*
## Exception Handling in [[Inheritance]]
### Example from HW: (layering)![[Figure 5 - Layering Exceptions.png]]
- Task: Push function should catch an ArrayException and throw a StackFullException (derived class of StackException)

> Uses [[STL Implementation]]
```
// Push function with exception
template <typename T>
void Stack<T>::Push(const T& element) {
	try {
		m_array[m_current] = element;
		m_current++;
	} catch (const ArrayException& e) { // Catch OutofBoundsException
	throw StackFullException();
	}
}
```

**StackException:**

```
#ifndef STACKEXCEPTION_HPP
#define STACKEXCEPTION_HPP
  
#include <string>

// Base class for stack exceptions
class StackException {
public:
	virtual std::string GetMessage() const = 0; // function for getting exception message
	virtual ~StackException() {} // Virtual destructor
};

// Exception for a full stack
class StackFullException : public StackException {
public:
	std::string GetMessage() const override {
		return "Stack is full.";
}

};

// Exception for an empty stack
class StackEmptyException : public StackException {
public:
	std::string GetMessage() const override {
		return "Stack is empty.";
}

};

#endif // STACKEXCEPTION_HPP
```

ArrayException (In Array.cpp)

```
// Array Implementation
...
...
...
// Base class for array exceptions
class ArrayException {
public:
	// Default constructor
	ArrayException() {}
	
	//Copy constructor
	ArrayException(const ArrayException& a) {}
	
	// Virtual destructor for proper cleanup of derived classes
	virtual ~ArrayException() {}
	
	// Pure virtual function to return the error message
	virtual std::string GetMessage() const = 0;
};

// Derived class for out-of-bounds exceptions
class OutOfBoundsException : public ArrayException {
private:
	int m_index; // The erroneous array index

public:
	// Default constructor
	OutOfBoundsException() : m_index(-1) {}

	// Constructor to initialize the erroneous index
	OutOfBoundsException(int error) : m_index(error) {}

	// Copy constructor
	OutOfBoundsException(const OutOfBoundsException& new_err) : m_index(new_err.m_index) {}

	// Override GetMessage to return a custom error message
	std::string GetMessage() const {
		return "Error: Index " + std::to_string(m_index) + " is out of bounds.";

}

};

}} // Closing namespaces

#ifndef Array_cpp

#include "Array.cpp" // Array.cpp is being preprocessed already (includeded in the hpp), this avoids multiple inclusion

#endif // ARRAY_CPP
  

#endif // ARRAY_HPP
```

- ALWAYS *throw the derived* class and *catch the base* class
- ArrayException is the base in this case (OutOfBoundsException is derived)
- StackException is the base class for *exceptions* and Full/Empty are it's derived



Back:: [[C++ MOC]]
tags:: #Programming 