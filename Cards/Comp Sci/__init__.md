up:: [[Python MOC]]
tags:: #Programming 
# Init
- This is a special method called constructor
- It is auto invoked when a new class is created ([[Classes in Python]])
- The primary purpose of the `__init__` method is to initialize the instance's attributes with the values passed to it
- The `__init__` method is crucial for setting up new objects with the necessary initial state, making it a fundamental part of object-oriented programming in Python
- Similar to a [[Default Constructor]] in [[C++ MOC]]
## Example
```class Book:
def __init__(self, title, author):
        self.title = title
        self.author = author

    def display_info(self):
        print(f"'{self.title}' by {self.author}")

# Creating an instance of Book
book1 = Book("1984", "George Orwell")

# Using the method
book1.display_info()  # Output: '1984' by George Orwell```
