up:: [[BOOST]]
tags:: #Programming 

# Smart [[Pointers]] 
- Pointers with automatic memory management
- `boost::shared_ptr<t>` 
	- Allows multiple smart pointers to own the same object
	- Use `std::shared_ptr` when objects are accessed or owned by multiple entities, and where the lifetime of the object is dependent on the existence of those multiple references.
- `boost::unique_ptr<>`
	- Has unique ownership of object it is points to
		- Only one unique_ptr for each object in memory
	- Can't be directly copied, can only transfer ownership via `std::move`
```
std::unique_ptr<Widget> copiedWidget = widgets[0];
// Can't do this (copy directly)

std::unique_ptr<Widget> copiedWidget = std::move(widgets[0]); 
// Transfer ownership

```
- Use `std::unique_ptr` when you need strict ownership semantics. This helps prevent ownership issues and makes the code easier to understand in terms of who owns an object at any given time.
## Example:

```
#include <boost/shared_ptr.hpp>
#include <iostream>
#include <vector>

// Assuming Shape is a base class for shapes like Circle, Rectangle, etc.
class Shape {
public:
    virtual void draw() const = 0; // Pure virtual function for drawing the shape
    virtual ~Shape() {
        std::cout << "Shape destroyed" << std::endl;
    }
};

class Circle : public Shape {
public:
    void draw() const override {
        std::cout << "Drawing Circle" << std::endl;
    }
};

class Rectangle : public Shape {
public:
    void draw() const override {
        std::cout << "Drawing Rectangle" << std::endl;
    }
};

// Typedef for a shared pointer to shape
typedef boost::shared_ptr<Shape> ShapePtr;

// For simplicity, using std::vector as the Array<T> class
typedef std::vector<ShapePtr> ShapeArray;

int main() {
    ShapeArray shapes;

    // Adding shapes to the array
    shapes.push_back(ShapePtr(new Circle()));
    shapes.push_back(ShapePtr(new Rectangle()));

    // Iterating over shapes and drawing them
    for (const auto& shape : shapes) {
        shape->draw();
    }

    // Shapes are automatically deleted when the shared_ptr's go out of scope
    return 0;
}
```
