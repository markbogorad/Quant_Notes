up:: [[BOOST]]
tags:: #Programming 
# Variants
- Part of [[STL Implementation]] since C++ 17
- Essentially the reverse of a [[Tuple]]: its a **type safe union**
- **Type safety**
	- Variants ensure that only one of the specified types can be stored at any time, and they provide mechanisms to check the stored type before accessing it. This **prevents type mismatches and runtime errors** associated with traditional unions.
- Memory efficient compared to [[Structs]]
#### Union:
 - Special data type that allows to store **different data types in the same location**
- All members share the same memory space
- Can hold 1 value out of a set of predefined types
```
union Data { 
	int i; 
	float f; 
	char c; 
};
```
- ##### Analogy:
	- Like a container, where the size of the container corresponds to the size of the largest thing in it:
		- Ex: using an old iPhone box to store an iPhone, keys, coins, etc, the size of the box is made for the iPhone but is used for other things too
## Usage
- Used in situations where variables may be one of several types but will only be one of those types for its lifetime in a given context.
	- **Function Returns:** Functions that might need to return values of different types based on their execution can use variants to encapsulate these return values safely.
	- **Parsing Data:** When reading data that can be of different types (e.g., from JSON or XML), a variant can store the parsed result without committing to a single type upfront.
	- **State Management:** In state machines or systems where an entity might be in one of several states represented by different types, variants can manage the current state in a type-safe manner.
## Example: C++ course level 8 ex 2
```
#include <boost/variant/variant.hpp>
#include <boost/variant/get.hpp>
#include "Shape.hpp"
#include "Line.hpp"
#include "Circle.hpp"
#include "Point.hpp"
#include "shapeVisitor.hpp"
#include <iostream>

using namespace Mark::CAD;
// Typedef for a variant
	typedef boost::variant<Point, Line, Circle> ShapeType;
// Function to create chape
	ShapeType CreateShape() {
	ShapeType shape;
	int choice;
	std::cout << "Choose a shape to create:\n1. Point\n2. Line\n3. Circle\n\nChoice: ";

	std::cin >> choice;

switch (choice) {
	case 1:
		shape = Point();
		std::cout << "Point chosen" << std::endl;
	break;
	
	case 2:
		shape = Line();
		std::cout << "Line chosen" << std::endl;
	break;
	
	case 3:
		shape = Circle();
		std::cout << "Circle chosen" << std::endl;
	break;

	default: 
	std::cout << "None Chosen" << std::endl;

	}

return shape;

}


int main() {

ShapeType shape = CreateShape();
std::cout << "\nVariant:" << std::endl;

try {
	Line& line = boost::get<Line>(shape); // Using global boost:get<T>() function
	std::cout << "Extracted a Line.\n";

} catch (const boost::bad_get& e) { // Throw boost::bad_get exception
	std::cout << "Error: The selected shape is not a Line.\n";

}

// Create a visitor instance
ShapeVisitor visitor(2, 4); // Move shape by (2, 4)

// 3 instances of ShapeType for point, line, and circle
	ShapeType shape1 = Point(0,0);
	ShapeType shape2 = Line(Point(0, 0), Point(1, 1));;
	ShapeType shape3 = Circle(Point(0, 0), 5);

// Display initial shapes
	std::cout << "\nInitial shapes:" << std::endl;
	std::cout << "Point at: " << shape1 << std::endl;
	std::cout << "Line at: " << shape2 << std::endl;
	std::cout << "Circle at: " << shape3 << std::endl;

// Apply visitor to move the shape
	boost::apply_visitor(visitor, shape1); // For point
	boost::apply_visitor(visitor, shape2); // For line
	boost::apply_visitor(visitor, shape3); // For circle

// Display moved shapes
	std::cout << "\nMoved shapes:" << std::endl;
	std::cout << "Point at: " << shape1 << std::endl;
	std::cout << "Line at: " << shape2 << std::endl;
	std::cout << "Circle at: " << shape3 << std::endl;
}
```

- Variant is used here to manage **shapes** within the CAD namespace
- Here, variant holds Points, Lines, and Circles within it's container
- **Applies [[Polymorphism]] without inheritance!**
	- The `ShapeVisitor` applied to the shapes via `boost::apply_visitor` demonstrates this. 
	- It allows **executing operations** (e.g., moving the shape) **on the contained shape regardless of its specific type**, akin to visitor pattern polymorphism but without requiring a shared base class.

Back:: [[BOOST]]