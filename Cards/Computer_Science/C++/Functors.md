up:: [[C++ MOC]]
tags:: #Programming
# Functors
- Aka **function objects**
	- Objects that are called as if they were functions
- Achieved by providing an overloaded () operator within a functor [[Class]] or [[Structs]]
- Unlike regular functions, functors can maintain state across calls because they can have data members.
	- Added capability of storing and manipulating internal state
## Example:

In this example, the `Increment` class defines a functor that adds a specified number (its state) to the number it's called with.

```
#include <iostream>

// Functor class definition
class Increment {
private:
    int num;
public:
    Increment(int n) : num(n) {}  // Constructor

    // Overload () operator
    int operator()(int i) const {
        return num + i;  // Add and return the result
    }
};

int main() {
    Increment inc(5);  // Create functor instance with state 5
    std::cout << inc(10);  // Calls the functor, output: 15
    return 0;
}

```
