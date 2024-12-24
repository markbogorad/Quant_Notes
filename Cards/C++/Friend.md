up:: [[Class]]
tags:: #Programming 
# Friend
## Purpose
- **Grants a function or another class access to a private member**
#### Limitations
- Not symmetrical
	- If class A declares class B as a friend, that doesn't mean class B has declared class A as a friend
- Not transitive
	- If Class A is a friend of Class B and Class B is a friend of Class C, Class A is NOT a friend of Class C
### Common uses
- [[Operator Overloading]]
- Unique class relationships

## Example:
```
#include <iostream>

class Box {
private:
    double width;

public:
    Box(double wid) : width(wid) {}

    // Declare a friend function
    friend void printWidth(const Box& b);
};

// Friend function definition
void printWidth(const Box& b) {
    // Direct access to private member
    std::cout << "Width of box: " << b.width << std::endl;
}

int main() {
    Box box(10.0);

    // Use friend function to print the width
    printWidth(box);

    return 0;
}

```