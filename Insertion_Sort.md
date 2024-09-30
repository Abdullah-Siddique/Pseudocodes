# Insertion Sort Algorithm

Insertion Sort is a straightforward sorting algorithm that builds a sorted array one element at a time. It is particularly efficient for small datasets or arrays that are already partially sorted. The algorithm works by dividing the array into a "sorted" and "unsorted" region, progressively growing the sorted region.

## How It Works

1. **Start with the Second Item:**
   - Assume the first item is sorted. Begin with the second element of the array.

2. **Insert into the Correct Position:**
   - Compare the current element (the "key") with the elements in the sorted portion of the array. Shift the larger elements one position to the right to make space for the key.

3. **Repeat for All Items:**
   - Continue this process for each subsequent element until the entire array is sorted.

## Pseudocode

The Insertion Sort algorithm can be represented in pseudocode as follows:
```
for i from 1 to n-1:
  key = array[i]
  j = i - 1
  while j >= 0 and array[j] > key:
    array[j+1] = array[j]
    j = j - 1
  array[j+1] = key
```

### Explanation of the Pseudocode:

- **Outer Loop (`i`):** This loop starts from the second element (index 1) and continues to the last element (index n-1) of the array. Each iteration considers the element at index `i` as the key to be inserted.

- **Key Assignment:** The current element `array[i]` is stored in `key`. This is the element we will insert into the sorted part of the array.

- **Inner Loop (`j`):** The inner loop compares the key with elements in the sorted portion. It runs while `j` is greater than or equal to `0` and the current sorted element `array[j]` is greater than `key`. If so, the current element is shifted one position to the right.

- **Insert Key:** Once the correct position is found (when `array[j]` is not greater than `key`), the key is placed at `array[j+1]`.

## Time Complexity

- **Worst-case and Average-case:** O(n²), where n is the number of items being sorted. This occurs when the array is sorted in reverse order.
- **Best-case:** O(n), which occurs when the array is already sorted.

## Conclusion

Insertion Sort is easy to implement and can be efficient for small datasets. It is an adaptive algorithm, meaning it becomes more efficient when sorting nearly sorted arrays. However, for larger datasets, more advanced algorithms like Merge Sort or Quick Sort are generally preferred due to their better performance.
