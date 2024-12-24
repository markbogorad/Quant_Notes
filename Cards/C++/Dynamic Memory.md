up:: [[C++ MOC]]
tags:: #Programming 
# Dynamic Memory
## What is it?
- Manually allocating and deallocating memory during the **runtime** of a program
- Requests memory on a need basis and releases it when no longer needed
- Stored on the Heap, (see [[Stack v Heap]])
## It's Purpose
- More efficient memory management
- Crucial for dealing with variables who's **size may not be known**
## Why it isn't standard:
- Takes more time (find open and suitable block of memory vs just put on stack)
- Can cause memory leaks (memory not being properly freed)
- Increases complexity of code
## In Contrast to Static Memory
- Static memory is allocating upon compile time on the stack
- For fixed size variables (no shrinking or growing arrays during runtime)
	- Does not adapt at runtime
## Usage
- Uses "new" and "delete" [[Operators]]
#### For a single object:
```
int* ptr = new int; // Allocates memory for an integer on the heap
*ptr = 5; // Assigns a value to the allocated memory
```
- Uses "new"
###### Deallocating the memory:
```
delete ptr; // Frees the allocated memory for the integer
```
- Uses "delete"
#### For array memory:
```
int* arr = new int[10]; // Allocates memory for an array of 10 integers
arr[0] = 1; // Assigns a value to the first element
```
- Uses "new"
###### Deallocating the memory:
```
delete[] arr; // Frees the allocated memory for the array
```
- Uses "delete"
### Best practices
- Always pair `new` with `delete` and `new[]` with `delete[]` to avoid memory leaks.
- Set pointers to `nullptr` after deallocating the memory they point to, to prevent dangling pointers.
- Consider using smart pointers (`std::unique_ptr`, `std::shared_ptr`, and `std::weak_ptr`) provided by the C++ Standard Library, which automatically manage memory and help prevent memory leaks and dangling pointers. Also a part of [[BOOST]]