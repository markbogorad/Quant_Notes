up:: [[C++ MOC]]
tags:: #Programming 

# Functions
- A function is a reusable code block designed to repeatedly execute a set of operations or functionalities throughout the program
- A function can take input in the form of parameters or arguments
	- Parameters: Placeholder for the values that the function will operate on and define the data type
	- Arguments: Actual values passed to the function when it's invoked. Assigned to the corresponding parameters

## Basic Syntax
```
dataType functionName (paramType1, paramName1, paramType2, paramName2 ...) {
	// Function body
	return value;
}

Ex:

// Fucntion for area of a cricle

double Circle::Area() const {
return M_PI * std::pow(radius, 2); // Formula here
}
```
# Commonly Used Functions 
- [[ToString]]
- [[Getters & Setters]]
- [[Mathematical Functions]]
- [[Inline Functions]]

## How to call in main
(put more stuff here)
1 example:

`int result = minus(a,b) // stores result of a - b in "result"`
where
`int minus(int a, int b) {return a - b;}