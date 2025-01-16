up:: [[Python MOC]]
tags:: #Programming 
# Self
- A conventional name for the 1st parameter of a class ([[Classes in Python]])
	- Refers to the instance of the class that is being created
	- *Think of `self` as a way for the methods in the class to say, "I am working on this particular object."*
- Allows instance methods to access attributes and other methods on the same object
- **Not a keyword** --> just a convention
- Equivalent of `this` in [[C++ MOC]]
## Example
```
class MyClass:
    def __init__(self, value):
        self.value = value

    def increment(self):
        self.value += 1

    def get_value(self):
        return self.value

```
- See [[__init__]]
