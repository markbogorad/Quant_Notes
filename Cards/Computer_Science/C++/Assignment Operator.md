up:: [[Canonical Header File]] , [[Operators]]
tags:: #Programming
# Assignment Operator
## Purpose
- Called when 2 objects of the same class are assigned to anything
	- ###### Ex(s): 
		- p2=p1
		- a=10, b=a
- Assigns value/variable from the right hand side of =
- Useful for making deep copies
## Declaration
```
Point& operator= (const Point& source);
```
- ##### const Point&
	- This is a constant **reference** to another object of the point class (of type point)
- ##### Operator=
	- Denotes the = operator is being overloaded here ([[Operator Overloading CPP]])
- ##### (const Point & source)
	- This is called a **parameter list**
		- ###### const 
			- -> constant function (will not modify the object), object here is Sourc
		- ###### Point& 
			- --> reference to the point object ([[Call by Reference]]
		- ###### Source 
			- --> arbitrary name given to the parameter that represents the new object (Source) that is being assigned to the current object (Point)

##### Declaration In Basic Words:
> When one `Point` object is assigned to another, take a constant reference to the object on the right-hand side of the assignment (source). Use its content to set the object on the left-hand side. Then, return a reference to the left-hand side object so that chain assignments can be performed."

## Implementation
```
Point& Point::operator=(const Point& source) {

// Self-assignment guard
	if (this == &source) {
	return *this;
}

// Copy the x and y coordinates from the source
	x = source.x;
    y = source.y;
return *this;

}
```
- ##### Self-Assignment guard
	- Checks if the object being assigned is not assigned to the same object (*this) 
		- This --> A [[Pointers]] to the object on which the member function is being invoked
	- == checks if the 2 have the same address (aka are the same)
	- If they are the same, the function will return immediately, otherwise it will proceed
- ##### Copy
	- These lines copy the x and y coordinates from the **source** object onto **this**
- ##### Return *this*
	- This returns the reference to the current object and allows for chaining assignment operations
## With [[Inheritance]]
```
Point& Point::operator=(const Point& source) {

// Self-assignment guard
	if (this == &source) {
	return *this;
}


// Call base class assignment operator
Shape::operator=(source); 



// Copy the x and y coordinates from the source
	x = source.x;
    y = source.y;
return *this;

}
```
- Need to call the **base class assignment operator** between self assignment guard and return commands