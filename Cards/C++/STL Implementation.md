up:: [[C++ MOC]]
tags:: #Programming
# STL
- STL has 4 main components:
## [[C++ Algorithms]]
- Includes common algorithms for sorting, searching, and manipulating data
## [[Containers]]
- Sequence containers:
	- Vector, list, deque
- Associative containers
	- set, multiset, map, multimap
- Container adaptors
	- Stack, queue, priority_queue
## [[Functors]]
- Encapsulates a function that can be passed won as an argument to another function
## [[Iterators]]
- Used to point to memory locations of STL containers
	- Similar to [[Pointers]]

## Implementation
- STL Implementation uses [[Templates C++]]
### Always define template prior to implementing a piece:
```
template <typename T>
...
// Implement your stuff
```
### New Colon Syntax
- Use the template to initialize:
```
// Default constructor

template <typename T>

Array<T>::Array() : m_size(10), m_data (new T[m_size]) {}; 

// Dynamically allocates memory for an array of type T with size 10
```
### Template Referencing
- Reference to an element of type T
```
const T& Array<T>::GetElement(int index) const {
...
// Implementation
}
```
- T&: 
	- This specifies a return type of T
	- References an object of type T
-  Array`<T>`::GetElement(int index) const:
	- Initializer list
		- Array`<T>` 
			- Specifies that GetElement is a method of the T template
		- int index
			- This method takes a single parameter "int index"
		- Const
			- Marked const here to not change the actual element (intended to be a getter)
### Linking
- Need to include the .cpp file at the end of the .hpp now:
```
#ifndef Array_cpp

#include "Array.cpp" // Array.cpp is being preprocessed already (includeded in the hpp), this avoids multiple inclusion

#endif // ARRAY_CPP

#endif // ARRAY_HPP
```
### Inheritance
- Derived classes are declared as follows:
```
template<typename T>
class NumericArray : public Array<T> {
public:
...
// Implementation
```
### Using templates to work with other classes:
- AKA template class specialization
- Not actually a template --> inherits from a template
#### EX:
```
class PointArray : public Array<Point> {
public:
...
// Implementation
...
```
- PointArray is a class derived from the **Array template class** (Array was made template typename T) and is specialized to store elements of the Point class
	- Point is the template parameter
- This class leverages all functionality of array but is explicitly designed to work with point objects
	- Here, its used to add additional functionality revolving around he Point object that Array itself does not provide
### Having templated classes interact (using one as a member of another)
- Define both classes under the same template
```
template <typename T>
class Stack {
private:
	int m_current; // Index for top of the stack
	Array<T> m_array; // Array to store elements
```
- Here, the array class (part of template T) is incorporated into the stack to use the functionality of Array in storing variables.
	- This is a case where it is not enough correlation in functionality to justify inheritance

Back:: [[C++ MOC]]
tags:: #Programming 