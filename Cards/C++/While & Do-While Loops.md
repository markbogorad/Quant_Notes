up:: [[C++ MOC]]
tags:: #Programming
# While Loop
- When iterations are not known before hand
	- Loop continues until a given condition is met
## In practice
```
while (condition) {
    // Block of code to be executed
}
```
#### Example:
```
int i = 0;
while (i < 5) {
    std::cout << i << " ";
    i++;
}
// Output: 0 1 2 3 4
```
- Initialize outside of loop
- While condition --> `i < 5`
- Increment within the implementation {brackets}

# Do-While
- Similar to while, except it guarantees the code block is executed at least once before condition is tested (checks the while expression)
	- This scenario is particularly useful when the **condition** that determines the **continuation** of the loop depends on **something that happens within the loop itself**
		- Ex: validating user input
- Basically:
	- Have an input --> see if you want to loop --> loop or don't loop
## In practice
```
do {
    // Block of code to be executed
} while (condition);
```
#### Example:
```
int i = 0;
do {
    std::cout << i << " ";
    i++;
} while (i < 5);
// Output: 0 1 2 3 4
```
- Process is in {brackets} after `do`
- Condition post brackets, then a semi colon
