up:: [[C++ MOC]]
tags:: #Programming 
# Struct
- Allows you to package different values into 1 entity
	- Very similar to a class
	- Key difference: 
		- Members of a struct are public by default
		- Members of a class are private by default
## When to use struct vs when to use class
- Use `struct` for **passive data structures** that mainly contain data and have **little or no functions/methods.****

- Use `class` for active data structures that encapsulate behavior (methods), especially those that require access control (private/protected members).

## Looks just like a class:
```
#include <iostream>
#include <string>

struct Person {
    std::string name;
    int age;
};

int main() {
	// Create an instance of the Person struct and initialize its members
	
    Person person1;
    person1.name = "Alice";
    person1.age = 30;

    // Accessing members of the struct to print
    std::cout << "Name: " << person1.name << ", Age: " << person1.age << std::endl;

    return 0;
}
```

