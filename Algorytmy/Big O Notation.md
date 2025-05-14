
![[Big O Notation.png]]
## Przykładowe struktury danych

| Data Structure      | Time Complexity |             |             |             |             |             |             |             | Space Complexity |
| ------------------- | --------------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ---------------- |
|                     | Average         |             |             |             | Worst       |             |             |             | Worst            |
|                     | Access          | Search      | Insertion   | Deletion    | Access      | Search      | Insertion   | Deletion    |                  |
| Array               | `Θ(1)`          | `Θ(n)`      | `Θ(n)`      | `Θ(n)`      | `O(1)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`           |
| Stack               | `Θ(n)`          | `Θ(n)`      | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`           |
| Queue               | `Θ(n)`          | `Θ(n)`      | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`           |
| Singly-Linked List  | `Θ(n)`          | `Θ(n)`      | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`           |
| Double- Linked List | `Θ(n)`          | `Θ(n)`      | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`           |
| Skip List           | `Θ(log(n))`     | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n log(n))`    |
| Hash Table          | `N/A`           | `Θ(1)`      | `Θ(1)`      | `Θ(1)`      | `N/A`       | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`           |
| Binary Search Tree  | `Θ(log(n))`     | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`           |
| Cartesian Tree      | `N/A`           | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `N/A`       | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`           |
| B-Tree              | `Θ(log(n))`     | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`           |
| Red-Black Tree      | `Θ(log(n))`     | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`           |
| Splay Tree          | `N/A`           | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `N/A`       | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`           |
| AVL Tree            | `Θ(log(n))`     | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`           |
| KD Tree             | `Θ(log(n))`     | `Θ(log(n))` | `Θ(log(n))` | `Θ(log(n))` | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`           |


## Sortowanie

| Algorithm      | Time Complexity |                  |                  | Space Complexity |
| -------------- | --------------- | ---------------- | ---------------- | ---------------- |
|                | Best            | Average          | Worst            | Worst            |
| QuickSort      | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n^2)`         | `O(log(n))`      |
| MergeSort      | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n log(n))`    | `O(n)`           |
| TimSort        | `Ω(n)`          | `Θ(n log(n))`    | `O(n log(n))`    | `O(n)`           |
| HeapSort       | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n log(n))`    | `O(1)`           |
| Bubble Sort    | `Ω(n)`          | `Θ(n^2)`         | `O(n^2)`         | `O(1)`           |
| Insertion Sort | `Ω(n)`          | `Θ(n^2)`         | `O(n^2)`         | `O(1)`           |
| Selection Sort | `Ω(n^2)`        | `Θ(n^2)`         | `O(n^2)`         | `O(1)`           |
| Tree Sort      | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n^2)`         | `O(n)`           |
| Shell Sort     | `Ω(n log(n))`   | `Θ(n(log(n))^2)` | `O(n(log(n))^2)` | `O(1)`           |
| Bucket Sort    | `Ω(n+k)`        | `Θ(n+k)`         | `O(n^2)`         | `O(n)`           |
| Radix Sort     | `Ω(nk)`         | `Θ(nk)`          | `O(nk)`          | `O(n+k)`         |
| Counting Sort  | `Ω(n+k)`        | `Θ(n+k)`         | `O(n+k)`         | `O(k)`           |
| CubeSort       | `Ω(n)`          | `Θ(n log(n))`    | `O(n log(n))`    | `O(n)`           |
