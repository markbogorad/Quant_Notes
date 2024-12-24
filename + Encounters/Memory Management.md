up:: [[Computer Science MOC]]
tags:: #Programming  
# Memory
## Hardware Context
- [[SSD]]
- HDD
- [[RAM]]
## Programming Context
- The efficient allocation, usage, and release of memory in a computer system
- Used in [[C++ MOC]]
	- [[Dynamic Memory]]
	- [[Smart Pointers]] have auto memory management in C++
### Memory Management Challenges
- **Fragmentation:** Occurs when free memory is scattered in small blocks, making it difficult to allocate large contiguous blocks of memory. It can be internal (within allocated memory) or external (in the free memory).
- **Memory Leaks:** Happen when allocated memory is not properly deallocated, leading to wasted memory that cannot be reused.
- **Double Free Errors:** Occur when a program tries to free the same memory block more than once, leading to undefined behavior or crashes.
- **Buffer Overflows:** When a program writes data beyond the boundaries of allocated memory, potentially causing data corruption or security vulnerabilities.