up:: [[Python MOC]]
tags:: #Programming 
# Dictionaries
- See [[Dictionaries]]
- In Python, a dictionary is an **unordered collection of key-value pairs**, where each key is unique. 
- Dictionaries are used to store data values in pairs, allowing you to quickly retrieve, update, and manage data.
## Key Methods
- `clear()`: Removes all items from the dictionary.
- `copy()`: Returns a shallow copy of the dictionary.
- `keys()`: Returns a view object containing the keys of the dictionary.
- `values()`: Returns a view object containing the values of the dictionary.
- `items()`: Returns a view object containing the key-value pairs of the dictionary.
- `update()`: Updates the dictionary with elements from another dictionary or an iterable of key-value pairs.
## Creating Dictionaries
```
# Using curly braces
my_dict = {
    "name": "Alice",
    "age": 25,
    "city": "New York"
}

# Using the dict() function
my_dict = dict(name="Alice", age=25, city="New York")

```
## Accessing Values
```
print(my_dict["name"])  # Output: Alice
print(my_dict.get("age"))  # Output: 25

# Using get() allows you to provide a default value if the key is not found
print(my_dict.get("country", "USA"))  # Output: USA

```

## Updating Entries
```
# Adding a new key-value pair
my_dict["country"] = "USA"

# Updating an existing key-value pair
my_dict["age"] = 26

print(my_dict)
# Output: {'name': 'Alice', 'age': 26, 'city': 'New York', 'country': 'USA'}

```
## Removing Entries
```
# Using del
del my_dict["city"]

# Using pop()
age = my_dict.pop("age")
print(age)  # Output: 26

# Using popitem() (removes and returns the last key-value pair)
last_item = my_dict.popitem()
print(last_item)  # Output: ('country', 'USA')

print(my_dict)  # Output: {'name': 'Alice'}

```
## Looping Through Dictionary
```
# Loop through keys
for key in my_dict:
    print(key)

# Loop through values
for value in my_dict.values():
    print(value)

# Loop through key-value pairs
for key, value in my_dict.items():
    print(key, value)

```
## Checking for Keys
```
if "name" in my_dict:
    print("Name is a key in the dictionary")
```
