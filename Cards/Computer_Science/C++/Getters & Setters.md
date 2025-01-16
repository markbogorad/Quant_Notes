up:: [[C++ MOC]]
tags:: #Programming

# Getters/Setters
- Getter --> gets the variable
- Setter --> sets the variable
## Purpose
- Primary purpose is to enhance [[Encapsulation]]
- Used to get/set private variables while keeping access hidden
- Getters and setters are typically overloaded to use less memory [[Operator Overloading]]

## Getter Declaration & Implementation
- Point here is to just **return the variable**
#### Ex: Point class (a double)
```
HPP)
	double x const;
	
CPP)
	double Point::X() const {
	return x;
}
```
- X was already a double type variable
- In the CPP, it's just given the name X and returns the double x in the body ({})
#### Ex: Line class (a Point variable "start" and "end")
```
HPP)
	Point Start() const;
	
CPP)
	Point Line::Start() const {
	return start;
}
```
- Here, since start is a point type variable, point is the prefix for what would otherwise be the same exact method as before
## Setter Declaration & Implementation
#### Ex: Point class (a double)
```
HPP)
	void x(double newX);
CPP)
	void x(double newX) { 
	x = newX; 
}
```
- Here, the original x double is set equal to the previously named instance of point (newX)
	- This has now **set** the variable for the program without directly touching it
#### Ex: Line class (a Point variable "start")
```
HPP)
	void Start(const Point& newStart); 

CPP)
	void Line::Start(const Point& newStart) {
		start = newStart;	
	}
```
- Using [[Call by Reference]] for the initializer list in newStart
- `start = newStart`
	- `newStart` is a unique parameter to the setter method, used to implement and set private variables


