up:: [[C++ MOC]]
tags:: #Programming 
# Switch-Case
- Control flow construct
- More than 2 options (vs [[If-Else Statements]] having true/false only)
## How it looks
```
switch (expression) {
    case constant1:
        // code to be executed if expression == constant1;
        break;
    case constant2:
        // code to be executed if expression == constant2;
        break;
    ...
    default:
        // code to be executed if expression doesn't match any case;
}
```
- Switch (expression): expression that goes here is whatever the cases will surround.
	- For example, if cases depend on a user input choice (as below), there would need to be a `int choice` declaration and switch would be `switch(choice)`
- **Break Statement:** It's important to include a `break` statement at the end of each case block (unless you intentionally want to use **fall-through**) to prevent unintentional execution of subsequent case blocks.
	- **Fall-through:** when 2 cases produce the same outcome and will use the same implementation `{}`
### Example of practical usage (input)
```
ShapeType CreateShape() {

int choice; // Choice integer for user selection

cout << "Choose a shape to create & move:\n1. Point\n2. Line\n3. Circle\n\nChoice: ";

cin >> choice; // input user selection

// Create and return shape based on user choice. Shapes are at default values (0,0)

switch (choice) {

case 1: return Point();

case 2: return Line();

case 3: return Circle();

default:

cout << "Invalid choice, defaulting to Point." << std::endl;

return Point();

}

}
```

#### Alternative: use the [[If-Else Statements]]
##### Pros of Switch-Case:
1. **Clarity for Discrete Values:** `switch` statements are ideal for checking a single variable against a series of constants. They can make the code cleaner and more readable when dealing with enumerated values.
2. **Potential Performance Benefit:** Some compilers optimize `switch` statements more efficiently than equivalent `if-else` chains, especially when the case values are dense, potentially using a jump table which results in faster execution.
3. **Fall-Through Logic:** `switch` statements allow for fall-through behavior (when the `break` statement is omitted), which can be useful for grouping multiple cases together that share the same block of code.
##### Cons Switch-Case:
1. **Limited to Equality Checks:** `switch` statements can only perform equality checks against discrete constants. They cannot handle ranges, inequalities, or logical combinations of multiple conditions.
2. **Limited to Integral or Enumerated Types:** The expression used in a `switch` statement must evaluate to an integral or enumerated type, limiting its use with other data types like floating-point numbers or classes (though C++17 allows `std::string`).
3. **Risk of Fall-Through Errors:** Accidental fall-through due to a missing `break` statement can lead to bugs that are hard to spot.