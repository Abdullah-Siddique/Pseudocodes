# Bubble Sort Algorithm

Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The process is repeated until the list is sorted. This algorithm is named for the way larger elements "bubble" to the top of the list.

## How It Works

1. **Compare Neighboring Items:** 
   - Start at the beginning of the array and compare the first two adjacent elements.
   
2. **Swap If Necessary:** 
   - If the first element is greater than the second, swap them.

3. **Continue for Each Pair:**
   - Move to the next pair of adjacent elements and repeat the comparison and swapping process.

4. **Repeat the Process:** 
   - After each pass through the array, the next largest element will have moved to its correct position. Continue the process until no swaps are needed, indicating that the array is sorted.

## Pseudocode

The Bubble Sort algorithm can be represented in pseudocode as follows:
```
for i from 0 to n-1:
  for j from 0 to n-1-i:
    if array[j] > array[j+1]:
      swap array[j] and array[j+1]
```

### Explanation of the Pseudocode:

- **Outer Loop (`i`):** This loop runs from `0` to `n-1`, where `n` is the number of elements in the array. It ensures that we pass through the array multiple times until it is sorted.
  
- **Inner Loop (`j`):** This loop runs from `0` to `n-1-i`. It compares each pair of adjacent elements and performs the necessary swaps. The `-i` is used to avoid re-checking the last `i` sorted elements, as they are already in their correct positions.

- **Comparison and Swap:** If the current element `array[j]` is greater than the next element `array[j+1]`, we swap them to move the larger element towards the end of the array.

## Example

Consider the array `[64, 25, 12, 22, 11]`:

1. **First Pass**:
   - Compare 64 and 25, swap: `[25, 64, 12, 22, 11]`.
   - Compare 64 and 12, swap: `[25, 12, 64, 22, 11]`.
   - Compare 64 and 22, swap: `[25, 12, 22, 64, 11]`.
   - Compare 64 and 11, swap: `[25, 12, 22, 11, 64]`.

2. **Second Pass**:
   - Compare 25 and 12, swap: `[12, 25, 22, 11, 64]`.
   - Compare 25 and 22, swap: `[12, 22, 25, 11, 64]`.
   - Compare 25 and 11, swap: `[12, 22, 11, 25, 64]`.
   - Compare 25 and 64, no swap needed.

3. **Third Pass**:
   - Compare 12 and 22, no swap needed.
   - Compare 22 and 11, swap: `[12, 11, 22, 25, 64]`.
   - Compare 22 and 25, no swap needed.
   - Compare 25 and 64, no swap needed.

4. **Fourth Pass**:
   - Compare 12 and 11, swap: `[11, 12, 22, 25, 64]`.
   - Compare 12 and 22, no swap needed.
   - Compare 22 and 25, no swap needed.
   - Compare 25 and 64, no swap needed.

5. **Fifth Pass**:
   - The array is now sorted as `[11, 12, 22, 25, 64]`, and no further swaps are needed.

The bubble sort algorithm continues until no swaps are made during a pass, indicating that the array is sorted.

## Time Complexity

- **Worst-case and Average-case:** O(n²), where n is the number of items being sorted. This occurs when the array is in reverse order.
- **Best-case:** O(n), which occurs when the array is already sorted.

## Conclusion

Bubble Sort is easy to understand and implement, making it a great choice for educational purposes. However, it is not the most efficient for large datasets. Other sorting algorithms like Quick Sort or Merge Sort are preferred in practical applications due to their better performance.
