up:: [[BOOST]]
tags:: #Programming 
## Static Cast
- Allows for conversion between types that are implicitly convertible, or in a few cases, for types where you have explicit conversion rules defined.
### Usage:
- **Converting between numeric types** such as from `int` to `float`, or `double` to `int`.
2. **Converting pointers** between classes in a hierarchy, such as from base class pointers to derived class pointers, provided there is a clear inheritance path.
3. **Invoking explicit constructor** or conversion functions defined in classes.

### Example:
```
double pi = 3.14159; 
int whole_part = static_cast<int>(pi); // convert double to int
```
