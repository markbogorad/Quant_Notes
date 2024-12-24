up:: [[C++ MOC]]
tags:: #Programming 
# Polymorphism
- Allows objects of different classes to be treated as **1 superclass**
- Refers to the ability of different objects to respond, each in its own way, to the same message (or method call). 
- A single function or method can operate on objects of multiple classes if those classes are derived [[Inheritance]] from the same base class or implement the same interface.
- Achieved through
	- Overloading
	- Overriding
### Example:
- A pointer of type "Animal" can point to instances of **Dog** or **Cat**, and calling a pointer ([[Pointers]]) **makeSound()** on it will invoke the respective method according to the actual object type (**Dog::makeSound()** or **Cat::makeSound()**).

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
#### Static Polymorphism
- [[Operator Overloading CPP]]
	- Operators can be changed and implemented differently
- Function overloading
	- Functions will preform differently depending on functions passed to them
#### Dynamic Polymorphism
- [[Overriding]]
	- Changing functions between derived and base classes in [[Inheritance]]
## Metaphor
- Imagine polymorphism in programming as a **universal remote** control for your electronic devices at home, like your TV, DVD player, and stereo system. Each device has its own specific functionality and controls, yet the universal remote can interact with any of them using a common interface. When you press a button on the remote, such as "Power" or "Volume Up," the remote knows how to communicate with the currently selected device to perform the desired action, *even though the underlying mechanism to change the volume on the TV is different from adjusting the volume on the stereo system*.
	- Universal remote: **the base class**
	- Electronic devices (TV, DVD, etc): **the derived classes**
	- Actions (ex: volume button) demonstrate the effects of polymorphism. The same remote (base class) will play out differently on each device (derived class) by using different functions (buttons)
