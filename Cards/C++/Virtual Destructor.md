up:: [[C++ MOC]]
tags:: #Programming 

# Virtual Destructor
## Purpose
- Used when objects are deleted through a pointer to the base class in [[Inheritance]]
	- Deleting the pointer itself might cause the destructor of the derived class not to get called
		- This would cause a resource leak
- By declaring a base destructor as virtual, you ensure that the derived class destructors are also called and the objects are deleted
- Only needed when
	- Class is intended to be a base class only
	- Want polymorphic behavior 
	- - The class is intended to be dynamically allocated and deallocated (e.g., using `new` and `delete`). [[Dynamic Memory]]

## Syntax:
```
class Base {
public:
    virtual ~Base() {
        // Cleanup code for Base
    }
};

class Derived : public Base {
public:
    ~Derived() {
        // Cleanup code for Derived
    }
};
```

