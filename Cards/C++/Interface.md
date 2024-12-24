up:: [[C++ MOC]]
tags:: #Programming 
# Interfaces
- This is a class with only pure virtual functions
## Example
```
class Interface {
public:
    virtual void method1() = 0; // Pure virtual function
    
    virtual void method2() = 0; // Pure virtual function
};
```

## What they are / purpose
- This is similar to an [[Abstract Base Classes]] except interfaces cant have member variables or concrete member functions
- Interfaces are used to define a **contract** for classes that implement them, ensuring they implement certain methods.  
- Classes implementing an interface must provide definitions for all pure virtual functions declared in the interface.  
- Interfaces are used for achieving **multiple inheritance** in C++.