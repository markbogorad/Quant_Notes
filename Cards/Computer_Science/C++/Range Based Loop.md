up:: [[C++ MOC]]
tags:: #Programming
# Range Based Loop
```
for (declaration : container) { // loop body }
```
- **Declaration**: This declares a variable that will be used to store each element of the container as the loop iterates. The type of this variable should match the type of elements stored in the container. You can also use `auto` to let the compiler deduce the type (see [[Data Types]] for auto.
	- This you declare at the loop to store your results basically, the container is the start and end point (what you traverse essentially)
- **Container**: This is the collection through which you are iterating. It can be an array, vector, list, or any other container that supports iterators. Needs to already exist and be instantiated
## Example:

![[Screenshot 2024-04-20 at 12.33.28 PM.png]]
