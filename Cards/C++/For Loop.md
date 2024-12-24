up:: [[C++ MOC]]
tags:: #Programming 
# For Loop
- Most standard loop
- Used when number of iterations ins known before entering the loop
## In practice
- 3 parts
	- Initialization
	- Condition
	- Increment/decrement
```
for (initialization; condition; increment) {
    // Block of code to be executed
}
```
#### Example:
```
for (int i = 0; i < 5; i++) {
    std::cout << i << " ";
}
// Output: 0 1 2 3 4

```
- Here, the loop goes:
	- Initialization at 0: int i = 0 
	- Condition: as long as i is less than 5
	- Increment/decrement: ++ is increment