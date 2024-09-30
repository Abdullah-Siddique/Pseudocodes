# Quick Sort Algorithm

Quick sort is an efficient sorting algorithm that sorts an array in ascending order. It employs a divide-and-conquer strategy to rearrange the elements in the array.

## How Quick Sort Works

1. **Choose a Pivot**: Select an element from the array as the "pivot". The choice of pivot can vary; it can be the first element, the last element, the middle element, or even a random element.

2. **Partitioning**: Rearrange the array so that all elements smaller than the pivot are on its left, and all elements greater than the pivot are on its right. The pivot is now in its correct position.

3. **Recursive Sort**: Recursively apply the above steps to the sub-arrays formed by splitting the original array into two parts: one with elements smaller than the pivot and the other with elements larger than the pivot.

## Pseudocode
```
if list has more than 1 item:
  pick a pivot
  partition the list into two: smaller and bigger than the pivot
  quicksort the smaller list
  quicksort the bigger list
```

## Example

Let's say we have the following array: `[10, 7, 8, 9, 1, 5]`

1. Choose a pivot, for example, `8`.
2. Partition the array into `[7, 1, 5]` (smaller than 8) and `[10, 9]` (greater than 8), with 8 in the middle.
3. Apply quick sort on the left `[7, 1, 5]` and right `[10, 9]` sub-arrays.
4. The process continues until all sub-arrays are sorted.

## Conclusion

Quick sort is a powerful sorting algorithm that, on average, performs better than other O(n^2) algorithms, such as bubble sort or insertion sort, making it a popular choice for sorting large datasets.
