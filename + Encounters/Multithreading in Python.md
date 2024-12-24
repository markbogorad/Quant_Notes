up:: [[Python MOC]]
tags:: #Programming 
# [[Multithreading]] in Python
- Executing multiple threads with a single process
## Example
```
import threading

def print_numbers():
    for i in range(5):
        print(f"Number: {i}")

def print_letters():
    for letter in 'abcde':
        print(f"Letter: {letter}")

# Create threads
thread1 = threading.Thread(target=print_numbers)
thread2 = threading.Thread(target=print_letters)

# Start threads
thread1.start()
thread2.start()

# Wait for threads to complete
thread1.join()
thread2.join()

print("Done")

```

In this example, `print_numbers` and `print_letters` are executed concurrently in separate threads.