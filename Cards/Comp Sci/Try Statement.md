up:: [[Python MOC]]
tags:: #Programming 
# Try Statement
- Used for [[Exception Handling]]

```
try:
    # Block of code to test for errors
except SomeException:
    # Block of code to handle the exception
else:
    # Block of code to execute if no errors occur (optional)
finally:
    # Block of code to execute regardless of whether an error occurs or not (optional)

```


## Ex:
```
try:
    # Trying to divide by zero, which will raise an exception
    result = 10 / 0
except ZeroDivisionError:
    # Handling the exception
    print("Cannot divide by zero!")

```