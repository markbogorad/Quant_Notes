up:: [[C++ MOC]]
tags:: #Programming 
# If Statements
- Control flow construct
- Preform a test and execute a block if that test is true/false
- Can be used for anything that results in a boolean
## How it looks:
```
int number = // some integer;

if (number > 0) {
    std::cout << "The number is positive." << std::endl;
} else if (number < 0) {
    std::cout << "The number is negative." << std::endl;
} else {
    std::cout << "The number is zero." << std::endl;
}
```

#### Alternative: use the [[Switch Case Blocks]]
##### Pros of If Else:
1. **Flexibility:** `if-else` statements can handle *complex logical conditions*, not limited to just equality checks. They can evaluate ranges, inequalities, and conditions involving multiple variables.
2. **Readability for Complex Conditions:** When dealing with intricate conditions, `if-else` statements can be more readable and straightforward.
3. **Type Independence:** `if-else` statements work with any data type that can be evaluated in a boolean context.
##### Cons of If Else:
 1. **Potentially Less Efficient for Simple Checks:** For a large number of simple equality checks, `if-else` chains can be less efficient than `switch` statements because each condition is evaluated sequentially until one is true.
2. **Verbosity:** For multiple discrete value checks, `if-else` chains can become verbose and harder to read compared to `switch` cases.