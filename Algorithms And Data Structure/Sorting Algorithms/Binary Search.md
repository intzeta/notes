Binary Search finds the index of the value within a **Sorted Array**.

- Firstly we create two indexes - Left and Right. Where left is equal to 0 and Right is equal to array.size() - 1;
- Then we iterate through the array with every call to the while loop being a division.
- The mid variable is defined with a formula to always be on the center of the divided array. The formula is: `Left border Index + ( Right Border Index - Left Border Index) / 2`.
- If the mid value is the number we are looking for we return it. Else if it's higher than the value we are looking for we divide the array by half to the left direction. Else we do it to the right direction. We also add or subtract one from the scope to "remove" the earlier mid value. 

```
int binarySearch(std::vector<int> array, int target) {
  int left = 0, right = array.size() - 1;
  while (left <= right) {
    int mid = left + (right - left) / 2;
    if (array[mid] == target) {
      return mid;
    } else if (array[mid] < target) {
      left = mid + 1;
    } else {
      right = mid - 1;
    }
  }
  return -1;
}
```