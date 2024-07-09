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


![[MergeSort1.excalidraw|100%]]

- In the merge function we declare the sizes of the Array's - Left and Right, and also the index's. The first while loop condition check if the Left And Right array's aren't overflowing. Then If the value in the left Array is lower or equal to the value in the Right Array we add the value to the array and index i, we add one to the Left Index and go to the next value.

- The 2 last while loops check if there are any left values. If yes it will add them to the array.

```
void merge(vector<int>& leftArray, vector<int>& rightArray, vector<int>& array){
    int LeftSize = leftArray.size();
    int RightSize = rightArray.size();
    int arrayIndex = 0, leftIndex = 0, rightIndex = 0;

    while(leftIndex < LeftSize && rightIndex < RightSize){
        if(leftArray[leftIndex] <= rightArray[rightIndex]){
            array[arrayIndex] = leftArray[leftIndex];
            leftIndex++;
        }else{
            array[arrayIndex] = rightArray[rightIndex];
            rightIndex++;
        }
        arrayIndex++;
    }

    while(leftIndex < LeftSize){
        array[arrayIndex] = leftArray[leftIndex];
        arrayIndex++;
        leftIndex++;
    }
    while(rightIndex < RightSize){
        array[arrayIndex] = rightArray[rightIndex];
        arrayIndex++;
        rightIndex++;
    }
}
```


![[MergeSort2.excalidraw|100%]]