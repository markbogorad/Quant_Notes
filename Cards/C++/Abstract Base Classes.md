up:: [[C++ MOC]]
tags:: #Programming 
# Abstract Base Class
- A class thats designed for the sole purpose of being a base class ([[Inheritance]])
## Purpose
- To provide a foundation upon which other classes can build, ensuring a certain level of uniformity and enforcing a contract for behavior among its subclasses.
## Characteristics
- Needs to contain 1 pure virtual function
	- Pure virtual function is a function that is assigned to 0 :
```
	virtual void draw() const = 0;
```
- Abstract base classes can't be instantiated [[Instantiation]]
	- Can't do baseClass::baseClass
- Derived classes **must** implement **all** virtual functions
	- Any class that inherits from an abstract base class must implement all of its pure virtual functions, or it will also become an abstract class and cannot be instantiated.
## How it looks (example)
```
#include <iostream>

// Abstract Base Class
class Shape {
public:
    // Pure Virtual Function
    virtual void draw() const = 0;
};

// Derived Class
class Circle : public Shape {
public:
    // Implementation of Pure Virtual Function
    void draw() const override {
        std::cout << "Drawing Circle" << std::endl;
    }
};

// Derived Class
class Square : public Shape {
public:
    // Implementation of Pure Virtual Function
    void draw() const override {
        std::cout << "Drawing Square" << std::endl;
    }
};

int main() {
    // Shape shape; // This would be illegal: cannot instantiate an abstract class
    Shape* shapes[2];
    shapes[0] = new Circle();
    shapes[1] = new Square();

    for (int i = 0; i < 2; ++i) {
        shapes[i]->draw(); // Polymorphic call to draw
    }

    // Cleanup
    delete shapes[0];
    delete shapes[1];

    return 0;
}
```

- You cannot create an instance of `Shape`, but you can use pointers or references of type `Shape` to interact with objects of its derived classes, such as `Circle` and `Square`.

- This allows for polymorphic ([[Polymorphism]]) behavior, where the type of the derived class determines which implementation of the `draw()` function is called.