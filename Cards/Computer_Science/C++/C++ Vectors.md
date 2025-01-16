up:: [[C++ MOC]]
tags:: #Programming
# Vectors
## Vectors
- **`std::vector`**: Represents a *dynamic array* that can grow or shrink in size. Offers fast random access to elements, efficient when adding or removing elements at the end. 
## Vector of [[Pointers]]
- Example: `std::vector<Widget*> widgetPointers;`
	- A vector designed to store pointers
### Creating Pointer Objects
```
for (int i = 0; i < 5; ++i) { 
widgetPointers.push_back(new Widget()); 
}
```
- Pushing back widget objects on to the widgetPointer vector, using [[Dynamic Memory]]
- In this code block, 5 widget objects are created dynamically and pushed back (stored) onto widgetPointers
- Must then be explicitly deleted:
```
for (auto ptr : widgetPointers) { delete ptr; }
```

#### Purpose:
- Memory management
- More efficient to rearrange the vector than directly modifying -> pointers use less space than copies
- Necessary for polymorphic behavior
-  