up:: [[C++ MOC]]
tags:: #Programming 
# Recursive Function
- A function that calls itself
	- Repeats its own behavior
## Common usage
- Sorting
	- quick sort
- Searching
	- Binary search in sorted array
- Traversing data structures
	- Trees, graphs
## In practice example (factorial formula):
```
#include <iostream>

int factorial(int n) {
    if (n == 0) { // Base case
        return 1;
    } else {
        return n * factorial(n - 1); 
	        // Recursive call
    }
}

int main() {
    int num = 5;
    std::cout << "Factorial of " << num << " is " << factorial(num) << std::endl;
    return 0;
}
```
- Typically use [[If-Else Statements]] or [[Switch Case Blocks]]
- Multiplying factorial within factorial if doesn't equal 0
## Must haves:
- A base case for recursion to end, without this you can have infinite recursion
	- Recursion should always progress to the base case
	- 