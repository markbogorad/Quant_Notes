up:: [[Python MOC]]
tags:: #Programming 
## Real-World Analogy: “Build Your Own Robot”

Imagine you're building a robot blueprint.
You want every robot to:
- have a name
- start with a battery level
- say “hello” when it boots

This is `__init__()`.

```python
class Robot:
    def __init__(self, name):
        self.name = name
        self.battery = 100
        print(f"{self.name} is now online!")
```

Now you create two robots:

```python
r1 = Robot("Optimus")
r2 = Robot("Wall-E")
```

Result:

```
Optimus is now online!
Wall-E is now online!
```

Each robot remembers **its own name** and starts with **its own battery = 100**.

---

## 🔥 Why Not Just Do This Outside `__init__`?

Because without `__init__`, you’d have to do stuff like this _manually_:

```python
r1 = Robot()
r1.name = "Optimus"
r1.battery = 100
```

And every time you forgot to set something, your program would break.

> `__init__()` automates this setup so that every object is _ready to go the moment it's created_.

---

## ❓ So What Does It Truly Do?

|Concept|Meaning|
|---|---|
|`__init__()`|Function that auto-runs when you create an object|
|`self.name = name`|Store the `name` _inside_ this object|
|`self.battery = 100`|Give each object its **own** starting battery|
|`print(...)`|You can run any other code during setup|

---

### 🧠 Recap: `__init__()` is Needed Because...

1. You want to make sure every object **starts with the right info**
    
2. You don’t want to repeat the setup code manually every time
    
3. You need each object to store **its own data** (not shared!)
    

---

Want me to show you how the same class behaves _with_ and _without_ `__init__()` so you can see the difference in use and errors?



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
