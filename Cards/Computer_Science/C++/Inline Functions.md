up:: [[C++ MOC]]
tags:: #Programming
# Inline Functions
## Purpose
- Optimization technique aimed at reducing function calls
- When a function is declared as `inline`, the compiler attempts to copy the function code instead of calling it each time
- The inline keyword is **merely** a suggestion, and may not be used by the compiler
	- Modern compilers might even use `inline` where not specified
- Its supposed to **increase efficiency** by removing function overheads that come with the traditional way of calling functions and **increase speed**
## Best practices
- Use inline functions for **small, frequently called functions,** such as accessor functions (getters and setters), and simple mathematical functions.
	- Avoid using `inline` for complex or lengthy functions.
- Trust the compiler's optimization abilities. Modern compilers are capable of making decisions about inlining functions, often obviating the need for explicit inlining.
## Example
```
inline int add(int x, int y) {
    return x + y;
}
```

