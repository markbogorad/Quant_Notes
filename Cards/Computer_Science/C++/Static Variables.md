up:: [[C++ MOC]]
tags:: #Programming
# Static Variables
- Intended to affect **storage duration of variables within functions**
- Lifetime of static variables extends throughout the lifetime of the program
	- No creating/destroying each time
		- Initialize once and value persists
- Declared inside a function (local static variable)
	- Scope of the variable is limited to that function
- Global static variable
	- Accessible from any function within the same file (but not function in other files)
		- Regular global variables have external linkage
## Usage
- Where you need a variable to remember its value across multiple invocations of a function 
- When you want to limit the scope of a global variable but ensure it remains available throughout the program execution
- Need to call static members via class declaration
- Ex: `myBook :: Edition(2)`
- where Edition is a static function