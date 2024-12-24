up:: [[C++ MOC]]
tags:: #Programming

# Mathematical Functions
- Used to implement mathematics
	- Typically the cmath library

## Example of a mathematical function:
- Lets calculate the area of a circle, given by:
$$
	 Area=πr^2
$$
- This would be done as follows:
### Declaration:
```
double Area() const;
```

### Implementation
```
double Circle::Area() const {
	return M_PI * std::pow(radius, 2);
}
```
- return M_PI
	- M_PI --> this is the value of Pi from cmath library
	- std::pow(radius, 2) --> this is saying radius^2