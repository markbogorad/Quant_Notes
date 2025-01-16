up:: [[C++ MOC]]
tags:: #Programming 
# Call by Reference
- Method of passing arguments to functions
- The function will receive the **actual** address of the object **not a copy** of its value
	- This modifies the actual object going forward
	- Vs pass by value, which makes a copy of whatever you pass
- In contrast to [[Pointers]]
- You can do operations directly on references
- Used to modify objects **indirectly**
	- Everything done to the reference object will be done to the actual object
	- Ex:
```
	int main() { 
	int x = 10; 
	int &ref = x; 
	ref++; 
	std::cout << "x = " << x << " and ref = " << ref << std::endl; 
	return 0; 
	}
```
- Here, the output is actually x = 11 and ref = 11, because the reference get's incremented and x is controlled by the reference (whatever happens to the reference happens to x), in contrast to Pointers

