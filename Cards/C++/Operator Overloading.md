up:: [[Operators]]
tags:: #Programming 
# Overloading
- Defining a new behavior for an operator relative to a custom type
	- Making an operator do something else
- Operator overloading is a type of [[Polymorphism]], in particular, Static Polymorphism

## General Implementation:
```
ReturnType ClassName::operatorX(ArgumentType argument) { 
// Implementation 
}
```

## Widely used overloads:
```
Point operator-() const
```
- declare a constant (-) operator

```
Point operator*(double factor) const;
```
- double factor --> parameter taken named factor of type double

```
Point operator+ (const Point& p) const;
```
- const in initializer list
	- point object P is also const
- All else the same

```
bool operator== (const Point& p) const; 
```
- bool --> True or false (boolean)

```
Point& operator*= (double factor);
```
- double factor --> parameter taken named factor of type double