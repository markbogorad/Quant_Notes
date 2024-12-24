up:: [[Computer Science MOC]]
tags:: #Programming  
# Binary Search
- Divide and conquer approach
-  A faster way to search for things by **halving**
	- Think of an example with people in a room:
		- Everyone pairs up and has a joint number 2. 1 person from each pari sits down, leaving the other person representing 2 people. Those pair up and repeat (loop)
- In practice:
	- Go to middle of list. Look if what you are searching for is greater on less than what was in the middle. Move to less than or greater than from that. See middle of that subsection and repeat
- ![[Pasted image 20240725160306.png]]
	
## Implementation in C
- Left and right variables are the bounds (low and high)
- Mid is created as the midpoint
- Start loop by looking for middle, branch the loop into left and right directions
`int binarySearch(const std::vector<int>& arr, int target) {`
    `int left = 0, right = arr.size() - 1;`
    `while (left <= right) {`
        `int mid = left + (right - left) / 2;
        `if (arr[mid] == target) {`
            `return mid;`
        `} else if (arr[mid] < target) {`
            `left = mid + 1;`
        `} else {`
            `right = mid - 1;`
        `}`
    `}`
    `return -1;`
`}`

`int main() {`
    `std::vector<int> arr = {2, 3, 4, 5, 9}; // Note: List must be sorted`
    `int target = 4;`
    `int index = binarySearch(arr, target);`
    `if (index != -1) {`
        `std::cout << "Element found at index " << index << std::endl;`
    `} else {`
        `std::cout << "Element not found" << std::endl;`
    `}`
    `return 0;`
`}`
