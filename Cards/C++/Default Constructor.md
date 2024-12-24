up:: [[Canonical Header File]]
tags:: #Programming
# Default Constructor
## Purpose
- Called when the class is created
- Initializes the classes objects
- This is where you initialize your declared variables (i.e public and private of class)
- Initialize at a starting point (ex: 0,0)
## Declaration
```
Point();
```
- Empty point instance
## Implementation

###### Ex: a Point class with private (X,Y) variables
```
Point::Point() : x(0.0), y(0.0) {}
```
- X and Y are initialized to doubles. 0 is used as this is a default initialization, essentially the starting point of the variables

###### Ex 2: a Line class using variables of another class (Point)
```
Line::Line() : Start(Point()), End(Point()) {}
```
- This initializes the **Start** member of the ==Line== class. **Start** is of type *Point* and *Point()* calls the default constructor of the *Point* class to make a *Point* object for the **Start** member

## With [[Inheritance]]
```
Line::Line() : Shape(), start(Point()), end(Point()) {}
```
- Just declare the base class (Shape in this case) right after the colon
