up:: [[Dynamic Memory]]
tags:: #Programming 
# Concept: Computer Memory

![[basic-example-drawio.webp]]
## The Stack
- Static memory storage
- Stores each variable by function in a LIFO order
- highly structured and auto managed by CPU
	- Makes it fast
- Auto memory allocation and deallocation
- Fixed size at start of program
- ###### Cons:
	- Limited space due to fixed size (large variables can make it overflow)
	- No resizing elements (can do this on the heap dynamically though)
## The Heap
- [[Dynamic Memory]] storage
- Directly managed by the programmer
- Can allocate large blocks of memory 
- Memory can be freed and reused multiple times throughout the program's execution.
- Allows for dynamic data structures like linked lists, trees, and resizable arrays.
- ###### Cons
	- Allocation and deallocation are more complex and slower due to manual management and the need to search for free blocks.
	- Can lead to memory leaks if not properly managed.
	- Fragmentation over time as blocks of memory are allocated and freed.
> Think of this as data made on the fly