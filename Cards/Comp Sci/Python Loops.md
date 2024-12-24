up:: [[Python MOC]]
tags:: #Programming 
# Loops
## For Loops
- iterate over a sequence (such as a list, tuple, string, or range)
```
for item in sequence:
    # block of code
```



- **Iterating over a list**
```
fruits = ["apple", "banana", "cherry"]
	for fruit in fruits:
    print(fruit)
# prints :
apple
banana
cherry
```

- **Iterating over a string**
```
for char in "hello":
    print(char)
# Prints : 
h
e
l
l
o
```

- **Iterating over a range**
```
for i in range(5):
    print(i)
# Prints:
0
1
2
3
4
```
- **Variations of range**
```
# range(stop) 
for i in range(5): 
	print(i) # Output: 0 1 2 3 4 

# range(start, stop) 
for i in range(2, 6): 
	print(i) # Output: 2 3 4 5

# range(start, stop, step) 
for i in range(1, 10, 2): 
	print(i) # Output: 1 3 5 7 9
```
## For Loops with Else Clause
- A `for` loop can have an `else` block, which is executed after the loop finishes normally (i.e., not interrupted by a `break`statement).
```
for i in range(5):
    print(i)
else:
    print("Loop finished successfully.")
```
