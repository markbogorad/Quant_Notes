up:: [[C++ MOC]]
tags:: #Programming
# Iterators
- A part of [[STL Implementation]]
- Similar to [[Pointers]] objects that [[C++ Algorithms]] use to traverse [[Containers]].
## Types of Iterators:
### Input iterator
- Reads 1 elements at a time in forward direction
### Output Iterator
- Writes 1 elements at a time in forward direction
### Forward Iterator
- Combines input and output iterators
### Bi-directional
- A forward iterator that can also move backwards
### Random Access Iterator
- Basically a jumpy bi-directional iterator

## Using Iterators Example:
- You don't initialize an iterator directly, instead you just give it a name (typically `it`) and the compiler will recognize it by it's member functions (like `.begin`)
```
// Test for sum of iterators function

cout << 

"Sum of all numbers in the vector using iterators: " << 

SumRange(doubleVector.begin(), doubleVector.end()) 

<< endl;
```
- Uses `.begin`, referring to 1st element in container, and `.end`, referring to 1 past the last element in the container
## const_interator
- Read only access to container's elements
	- Useful when you want to ensure you don't change anything in the containers data
### Usage:
```
#include <iostream>
#include <vector>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    for (std::vector<int>::const_iterator it = vec.cbegin(); it != vec.cend(); ++it) {
        std::cout << *it << " ";
        // *it = 10; // This line would cause a compile-time error
    }
    // Output: 1 2 3 4 5

    return 0;
}
```
## Useful for loops, example:
```
for (it = numbers.begin(); it != numbers.end(); ++it) { 
std::cout << *it * 10 << std::endl; 
}
```
- For loop:
	- Initialize iterator from beginning of the numbers vector and the loop continues as long as the iterator does not equal the end of the numbers vector
- To access the iterator's value, you need to dereference it (`*it`)
	- Or use a pointer it -> getS
- This multiplies each element of the vector by 10