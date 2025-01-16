up:: [[C++ MOC]]
tags:: #Programming 
# Inheritance
- **Inheritance enables [[Polymorphism]]** **and uses** [[Colon Syntax]]
- Inheritance is a mechanism that allows a class (called the child or derived class) to inherit properties and behaviors (methods and fields) from another class (called the parent or base class). It's a way to form a hierarchical relationship between classes, enabling the reuse of common logic and introducing a hierarchical organization of classes.
	- Code reuse and hierarchical relationship
###### Example: 
- **Inheritance:** **Dog** and **Cat** classes inherit from **Animal**.
- Same example as [[Polymorphism]] (animal noises)

```
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    // Virtual function in the base class
    virtual void makeSound() const {
        cout << "This animal makes a generic sound." << endl;
    }
};

// Derived class Dog
class Dog : public Animal {
public:
    // Override the makeSound function for Dog
    void makeSound() const override {
        cout << "Dog barks: Woof!" << endl;
    }
};

// Derived class Cat
class Cat : public Animal {
public:
    // Override the makeSound function for Cat
    void makeSound() const override {
        cout << "Cat meows: Meow!" << endl;
    }
};

int main() {
    Animal* myAnimal;
    Dog myDog;
    Cat myCat;

    // Pointing to Dog
    myAnimal = &myDog;
    myAnimal->makeSound(); // Output: Dog barks: Woof!

    // Pointing to Cat
    myAnimal = &myCat;
    myAnimal->makeSound(); // Output: Cat meows: Meow!

    return 0;
}
```

## New Access Specifier : Protected
- One more access specifier (private and public) for inheritance: **Protected**
- Used in inheritance only
![[Screenshot 2024-03-20 at 12.33.14 PM.png]]
###### Protected members can be used only by the following:
- Member functions of the base class.
- Member functions of friends of the base class.
- Member functions of derived classes of the base class. 
- Friends of the derived class.
## Purpose:
- The primary reason for using protected access is t**o allow a base class to share its members with classes that inherit from it**, without making those members available to the rest of the program. 
	- This is useful for when you want to keep some aspects of your class internal to a family of related classes but not entirely private to the class where they are declared.
- Basically the private type + access to derived classes
	- **Public Members** are accessible from any part of the code.
	- **Protected Members** are accessible within the class, by derived classes, and by friends.
	- **Private Members** are accessible only within the class itself and by friends.


