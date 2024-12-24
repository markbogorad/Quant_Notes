up:: [[C++ MOC]]
tags:: #Programming
# Arrays
- A way to store fixed size sequential elements of the same type
- **Fixed Size**: determined on creation and cant change in runtime
- **Homogenous:** all elements within the array must be the same type
- **Contiguous Memory Allocation:** An array allocates memory for its elements in a contiguous block of memory. 
- This means that the elements are stored in adjacent memory locations, which allows for efficient access and manipulation of array elements using indexing.
- If size is known, use array. If size is unknown, use [[C++ Vectors]]
## Declaration
``int myArray[10]; // Declares an array of 10 integers``
## Initialization
- Most commonly done via loops [[For Loop]]

Simple input
``int myArray[5] = {1, 2, 3, 4, 5}; // Initializes an array of 5 integers
or input like this:
`int myArray[5];`
`myArray[1] = 2;
- If you don't initialize an array explicitly, its elements are uninitialized (contain garbage values). 
- If you initialize fewer elements than the size of the array, the rest of the elements are default-initialized (zero for fundamental types).
## Accessing Elements
- Uses `[]` operator:
`int firstElement = myArray[0]; // Accesses the first element of the array`
- Modifying parts of the array
`myArray[3] = 10; // Modifies the fourth element of the array`
- 3 is 4th element (they initialize at 0)
## Matrices (multidimensional arrays)
```
int matrix[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```
### Limitations and Considerations
- **Fixed Size:** The static nature of arrays (fixed size) can be limiting. For dynamic collections of elements that can grow or shrink, C++ offers container classes like `std::vector`.
- **Safety:** C++ does not perform bounds checking on arrays. Accessing an array out of its bounds can lead to undefined behavior, such as accessing or modifying data held in other parts of your program.
### Pros of arrays vs vectors
- Arrays can be faster --> worthwhile if you don't intend on changing size
- Size predictability can actually benefit code
## Relationship to [[Pointers]]
- **Points to elements (index) not values**
- An array name can be considered as a constant pointer pointing to its first element. 
- This allows you to perform pointer arithmetic based on the array:
`int arr[5] = {10, 20, 30, 40, 50};` 
`int* ptr = arr; // Pointer to the first element`
`std::cout << *(ptr + 1); // Outputs: 20`
## Dynamic Array
- Stored on the heap
	- [[Stack v Heap]]
	- [[Dynamic Memory]]
### Example:
```
int* dynamicArray = new int[10]; // Stored on heap
// Use the array...
delete[] dynamicArray; // Memory must be freed
```
## Array [[Exception Handling]]
- When the array is out of bounds
- C++ doesn't have automatic array exceptions
	- Need to implement
- Can do it with an [[If-Else Statements]] or **Try-Catch Blocks**
### If-else style implementation:
```
void safeAccess(int* array, int index, int size) { 
	if (index < 0 || index >= size) { 
	throw std::out_of_range("Index is out of range."); 
} 
	std::cout << "Accessing element: " << array[index] << std::endl; }
```
##### Parameters:
- `int* array`: A pointer to the first element of an integer array. This pointer represents the array to be accessed.
- `int index`: The position in the array that the caller wants to access.
- `int size`: The total number of elements in the array.
##### Function Body:
1. **Range Check:**
    - if (index < 0 || index >= size)
	    - If the index is less than 0 or more than specified `size`, it will be out of bounds
2. **Throwing an Exception:**
    - If out of range --> throw `std::out_of_range` 
    - If not caught terminate the program
1. **Accessing the Element:**
    - If the index is within the valid range, the function proceeds to access the array element at the given index.
	    -  `std::cout` showing element accessed.
    - `array[index]` accesses the element at the specified index in the array.
### Try-Catch Blocks
```
// Push function with exception
template <typename T>
void Stack<T>::Push(const T& element) {
	try {
		m_array[m_current] = element;
		m_current++;
	} catch (const ArrayException& e) { 
	// Catch OutofBoundsException (hiding array)
		throw StackFullException();
}
```
- Try: attempt to add `element` to the current position in the array (`m_current`) and set this equal to element again ([[Recursive Function]]). 
	- This will not work if put of bounds, so the `catch` block will catch an exception class and throw a full exception message (via another class)

Back:: [[C++ MOC]]
tags:: #Programming 