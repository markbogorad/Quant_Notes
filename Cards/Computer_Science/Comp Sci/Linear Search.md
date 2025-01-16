up:: [[Computer Science MOC]]
tags:: #Programming  
# Linear Search
- Checks each element of an array 1-by-1 until element is found
	- Not very efficient
- ![[Pasted image 20240725160157.png]]
	
## Implementation in C
- Basically loop through an array and if you get what you want end the loop

`int linearSearch(const std::vector<int>& arr, int target) {`
    `for (int i = 0; i < arr.size(); ++i) {`
        `if (arr[i] == target) {`
            `return i;`
        `}`
    `}`
    `return -1;`
`}`

`int main() {`
    `std::vector<int> arr = {3, 5, 2, 4, 9};`
    `int target = 4;`
    `int index = linearSearch(arr, target);`
    `if (index != -1) {`
        `std::cout << "Element found at index " << index << std::endl;`
    `} else {`
        `std::cout << "Element not found" << std::endl;`
    `}`
    `return 0;`
`}`
