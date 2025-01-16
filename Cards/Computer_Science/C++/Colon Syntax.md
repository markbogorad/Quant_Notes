up:: [[C++ MOC]]
tags:: #Programming
# Colon Syntax
### AKA the member initializer list

#### Colon Syntax in [[Inheritance]]
```
class DerivedClass : public BaseClass {
// implementation
}
```
- Colon splits the derived class declaration and uses the colon to show base class inheritance
###### Initializing in Inheritance
```
// Copy constructor colon syntax
Point::Point(const Point& p) : Shape(), x(p.x), y(p.y) {}
```
- Shape is used after colon to show inheritance from base class
#### Colon Syntax in initialization
- Allows for the direct initialization of variables before the constructor's body is executed
- General format --> **Deceleration : Initialization**
```
ClassName::Classname (Type1 param1, Type2 param2) : member1(param1), member2(param2)
```
- 1st ClassName
	- Defines a function as a member of class name
- 2nd ClassName
	- Name of the constructor (same as class)
- (Type1 *param1*, Type2 *param2*)
	- Parameters of the constructor
		- Type1 *param1
			- This just means a parameter of type 1
				- Ex: double *x*, double *value*
- Colon splits **declaration** and **initialization**
- member1(*param1*)
	- Initializes member1 with value of param1

##### Pros of Colon Syntax
- Directly initializes members without calling default constructor (more efficient)
- Allows for existence of "const" members, which can only be made on creation
##### Alternative: Direct initialization
```
ClassName::ClassName() {
variable = value
}
```