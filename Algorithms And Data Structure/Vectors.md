#### Popular functions and methods of std::vector

- `vector.push_back(value)` - Insert a new element at the end of a vector
- `vector.front()` - Access the first element of the vector
- `vector.back()` - Access the last element of the vector
- `vector.size()` - Returns the numbers of elements in a vector
- `vector.begin()` - Returns a iterator to the beginning. (Used in vector.sort() function)
- `vector.end()` - Returns a iterator to the end. (Used in vector.sort() function)
- `vector.empty()` - Check if the vector is empty, returns bool.


#### Using the vector

- Iterating through every element and checking if it's the same. Time Complexity - `O(n^2)`
  This code is used in the question "Two Sum" on LeetCode and it's a BruteForce Example: 
```	
for (int i = 0; i < vector.size() - 1; i++) {
	for (int j = i + 1; j < vector.size(); j++) {
	    if (nums[i] + nums[j] == target) {
	        return {i, j};
	    }
	}
}
```

