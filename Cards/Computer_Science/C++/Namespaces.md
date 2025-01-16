up:: [[C++ MOC]]
tags:: #Programming
# Purpose
- Namespaces are used for grouping entities (classes), especially within a large file
## Defining a namespace
```
namespace contracts {

// class delceration {


}

} // closing namespace
```
- Here, a simple namespace "contracts" is created
- Closing the namespaces is 2nd last thing in the file (before "#endif")

## Namespace within a namespace
```
namepsace contracts {
namespace options{

// class decleration {

}

}} // CLosing namespaces
```
- Here, an options namespace is specified within the contracts namespace

# Using namespaces
- Used when you need to access a member within a namespace

## 2 Methods:

### At the top of file:
- Done with the using directive
- More efficient (don't need to do a million colons each time)

```
using namespace contracts

// or

using namespace contracts::options
```

### Within implementation:
- Useful to know where it came from
- Also useful for 1-off uses of the namespace

```
in main () {
	// Accessing a previously defined function from "option class"
	contracts::options::callFunction; 
	
	// Accessing a variable from options class
	int x = contracts::options::value; 
	
	// Creating an object of the "call" class
	contracts::options::call obj 
}
```