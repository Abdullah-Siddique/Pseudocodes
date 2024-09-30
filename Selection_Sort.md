# Selection Sort Algorithm

Selection sort is a straightforward and intuitive sorting algorithm used to arrange an array in ascending order. It works by repeatedly finding the smallest element from the unsorted portion of the array and moving it to the beginning.

## How Selection Sort Works

1. **Find the Smallest Item**: Start from the first element of the array and search for the smallest item in the entire array.

2. **Swap with the First Item**: Once the smallest item is found, swap it with the first element of the array.

3. **Repeat for Remaining Items**: Move to the next position and repeat the process: find the smallest item from the remaining unsorted portion and swap it with the element at the current position.

4. **Continue Until Sorted**: This process continues until the entire array is sorted.

## Pseudocode

```
for i from 0 to n-1:
  smallest = i
  for j from i+1 to n-1:
    if array[j] < array[smallest]:
      smallest = j
  swap array[i] and array[smallest]
```

## Example

Consider the array `[64, 25, 12, 22, 11]`:

1. **First Iteration**:
   - Find the smallest item (11) and swap it with 64: `[11, 25, 12, 22, 64]`.

2. **Second Iteration**:
   - Find the next smallest item (12) and swap it with 25: `[11, 12, 25, 22, 64]`.

3. **Third Iteration**:
   - Find the next smallest item (22) and swap it with 25: `[11, 12, 22, 25, 64]`.

4. **Fourth Iteration**:
   - The last two elements (25 and 64) are already in order, so no swap is needed.

## Conclusion

Selection sort is simple and easy to implement but is inefficient on large lists, making it less suitable for larger datasets compared to more advanced algorithms like quick sort or merge sort. Its time complexity is O(n²), which is due to the nested loops for searching the smallest element.
