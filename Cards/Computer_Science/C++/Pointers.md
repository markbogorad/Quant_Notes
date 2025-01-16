up:: [[C++ MOC]]
tags:: #Programming 
# Pointers
[Fetching Title#vmq3](https://www.youtube.com/watch?v=i49_SNt4yfk&t=1s)
 ![Pointers](https://youtu.be/i49_SNt4yfk?si=IyT8pUzivdofIPt8)
---
## An Analogy
> Imagine computer memory as a long row of houses, all having their own address. Pointers are a way for packages to be delivered to each of these houses addresses.
## Some Definitions
- #### Pointer
	- A variable (number) that stores the memory address of another variable
	- ###### EX:
		- Int* x 
			- The * is attached to the type declaration but actually signals the beginning of a pointer called **x** to an int type
		- x* = 42
- #### Pointee
	- Thing that the pointer points to
	- Thing thats getting pointed on
- #### Dereferencing
	- Direct accesses the pointee
		- **Allows for modification by the pointer to the original** 
	- Accessing the memory address of the other variable
	- Uses the * operator ([[Operators]])
## 3 Pointer Rules
- A pointer points to a pointee but they are **separate**
	- Common error: forgetting to give a pointer a pointee (thing to point to)
- Dereferencing starts at the pointer and follows over to access the pointee
	- Again, must have a pointee
- Pointer assignment takes a pointer and changes it to point to the same thing as the other pointer
	- ###### EX:
		- y* = 10
		- x* = y*
			- x* now also points to 10
## In Practice 
### Pointer Initialization
```
int var = 10; // Variable var
int* ptr = &var; // a pointer variable "ptr" that holds the address of var (ptr becomes 10)
```
- ptr now points to the address of var (it becomes 10)
### Dereferencing
```
int value = *ptr; // Read the value of the variable "var" through ptr
*ptr = 20; // Modify the value of var through ptr
```
- Dereferencing with * operator
- New variable "value" enters, taking the 10 thats being pointed by ptr
- ptr = 20 --> directly modifying the pointer, and in turn, the "var" variable

### Null Pointers
```
int* ptr = nullptr; // Using nullptr to initialize a null pointer (C++11 onwards)
```
- Does not point to any specific location
- Used to initialize pointers when *no actual memory address is intended to be assigned yet***
- Can't dereference a nullptr

### Pointer Arithmetic
```
int arr[] = {10, 20, 30}; // Array is created
int* ptr = arr; // Points to the first element of arr
++ptr; // Now points to the second element of arr
```
- Arithmetic operations on pointers are allowed
	- ++ is used here to go on to the next index of the array

### Pointer to a Pointer (irrelevant for QN course)
```
int** pptr = &ptr; // pptr is a pointer to a pointer to an integer
```
- ###### Usage:
	- Dynamic array of pointers
		- Used to dynamically allocate an array of pointers
	- Multidimensional arrays
	- Pass by pointer

### [[Dynamic Memory]] Management
```
int* ptr = new int; // Dynamically allocate memory for an integer
*ptr = 5; // Assign a value to the allocated memory
delete ptr; // Free the allocated memory
```
- "new" operator ([[Cards/C++/Operators]])
- "delete" operator ([[Cards/C++/Operators]])

## "This" Pointer
- Special keyword representing a pointer to an object on which a member function is being invoked
	- A way to refer to the calling object itself
### Uses:
#### Accessing members
- Member variables of the object
	- `This` is useful when variable and parameter has the same name
- Here, int value is being invoked on example, returning value
```
class Example {
public:
    int value;
    Example(int value) {
        this->value = value; 
// Sets the member variable 'value' to the parameter 'value'
    }
};

```
- Parameter from example (int value) and variable is the int
#### Returning `*this` 
- When you need to use a partially edited version of a member mid code
- `*this` is a dereferenced pointer on the calling object
- Useful for **chaining method calls** on one object
```
class Counter {
private:
    int count;
public:
    Counter() : count(0) {}

    Counter& increment() {
        ++count;
        return *this; // Return the dereferenced this pointer (the object itself)
    }

    int getCount() const {
        return count;
    }
};

// Usage
Counter c;
c.increment().increment(); // Chaining calls

```
- Here, the dereferenced `*this` pulls out an incremented version of `counter` with an `increment` function
- `Increment` can be used to chain methods by using it multiple times in `usage`

Back:: [[C++ MOC]]