up:: [[Python MOC]]
tags:: #Programming 
# Class Structure in Python
- Use a colon to start the class
	- ex --> `class BlackScholes:`
- Use `def` keyword to define methods
	- In [[C++ MOC]], this is all within the braces `{}`
- All methods are `public` by default
	- In [[C++ MOC]] [[Class]]es, methods can be public, private, or protected ([[Encapsulation]])
	- To make private in python:
		- Use a convention (prefixing with an underscore) or name mangling (prefixing with double underscores).
- Constructors:
	- Python: The constructor method is always named [[__init__]]and uses [[Calling "Self" in Python]] to refer to instance attributes.
	- C++: The constructor has the same name as the class and uses `this` to refer to instance attributes. ([[Default Constructor]])
- Destructors
	- Python has auto garbage collection, no need. Official method is `__del__`
- Memory management is automatic
## Example
```
class MyClass:
    def __init__(self, value):
        self.value = value  # Instance variable

    def increment(self):
        self.value += 1

    def get_value(self):
        return self.value

# Creating an instance of MyClass
my_instance = MyClass(10)
print(my_instance.get_value())  # Output: 10
my_instance.increment()
print(my_instance.get_value())  # Output: 11
```
