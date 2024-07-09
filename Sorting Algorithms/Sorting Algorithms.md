#### Bubble Sort O(n^2)




#### Merge Sort O(n log n) [[Big O Notation]]

- Merge sort is done by dividing the Array into smaller part - Left Array and Right Array, until they are all only 1 element. We are doing it through **recursion**.

- In the code below we set the base condition to check if the array is only one element, else we create a new vector **"Left Array"** and **"Right Array"** and set their value corresponding to the side they are on (For Left Array we're doing the first half and for the Right Array the next half). And on the end we call the other function to divide your Array's even more.

-  If the Array is only 1 element we comeback to the previous function and call the merge function that will reconnect the rearrange the array.

```
void mergeSort(std::vector<int>& array){
    if(array.size() <= 1) return; 

    int middle = array.size() / 2;
    std::vector<int> leftArray(array.begin(), array.begin() + middle);
    std::vector<int> rightArray(array.begin() + middle, array.end());
 
    mergeSort(leftArray);
    mergeSort(rightArray);
    merge(leftArray, rightArray, array);
}
```


![[MergeSort.excalidraw|100%40]]