up:: [[Polymorphism]]
tags:: #Programming 
# Overriding
- Changing the usage of a particular function from the Base class onto derived classes
## Ex:
```
#include <iostream>

class Animal {
public:
    // Virtual function in the base class
    virtual void speak() const {
        std::cout << "This animal speaks an unknown language." << std::endl;
    }
};

class Cat : public Animal {
public:
    // Overriding function in the derived class
    void speak() const override {
        std::cout << "Meow" << std::endl;
    }
};

int main() {
    Animal* myAnimal = new Cat();
    myAnimal->speak(); // Calls the overridden function in Cat

    delete myAnimal;
    return 0;
}

```
- Here, the base class `speak` function is overridden to output a specific line in relation to the derived
	- I.E. it outputs "Cat goes Meow" instead if "Animal speaks unknown language"
## Ground Rules
- Base class function must be declared `virtual`
- Derived class function must end with `override`