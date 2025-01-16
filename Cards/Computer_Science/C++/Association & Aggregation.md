up:: [[C++ MOC]]
tags:: #Programming 
# Association & Aggregation
- These are both terms describing relationships between classes
- These are purely concepts
## Association
- This describes a relationship where one class uses or interacts with objects of another class
- Typically implemented by having a member variable in a class that holds a reference or a pointer to the object(s) of another class.
- Can be
	- Bidirectional (both classes interact with each other)
	- Unidirectional (one class interacts only)
- Example:
```
class Professor {
    // ...
};

class Department {
private:
    Professor* advisor;
public:
    Department(Professor* p) : advisor(p) {}
    // ...
};

```
- **Department** has unidirectional association with **professor** because it holds an object of **professor**
## Aggregation
- AKA whole-part pattern
	- There can be a fixed amount of parts in the whole
- Specialized form of association 
	- No strong ownership of derived class from base class
- Example:
```
class Engine {
    // ...
};

class Car {
private:
    Engine* engine; // Car has-an Engine
public:
    Car(Engine* e) : engine(e) {}
    // ...
};
```
- Here, `Car` aggregates `Engine`. The `Car` object contains an `Engine`, but the `Engine` can exist without the `Car`.



back:: [[C++ MOC]]