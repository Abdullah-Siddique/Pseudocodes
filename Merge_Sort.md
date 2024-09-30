# Merge Sort Algorithm

Merge Sort is a powerful and efficient sorting algorithm that follows the divide-and-conquer paradigm to sort an array in ascending order. This algorithm works by recursively dividing the array into smaller halves until each piece contains a single element. Then, it merges the pieces back together in the correct order. 

## How Merge Sort Works

1. **Divide**: If the list has more than one item, split the list into two halves.
2. **Conquer**: Recursively apply the merge sort to both halves of the list.
3. **Merge**: Combine the two sorted halves back together into a single sorted list.

## Pseudocode

The following pseudocode outlines the steps of the merge sort algorithm:
```
function merge_sort(list):
    if length of list > 1:
        mid = length of list / 2
        left_half = list[0:mid]          // First half of the list
        right_half = list[mid:length of list] // Second half of the list

        merge_sort(left_half)            // Recursively sort the first half
        merge_sort(right_half)           // Recursively sort the second half

        merge(left_half, right_half, list) // Merge the sorted halves

function merge(left_half, right_half, list):
    i = 0 // Index for left_half
    j = 0 // Index for right_half
    k = 0 // Index for the merged list

    // Merge elements from left_half and right_half in sorted order
    while i < length of left_half and j < length of right_half:
        if left_half[i] < right_half[j]:
            list[k] = left_half[i]     // Assign the smaller element to the merged list
            i = i + 1                   // Move to the next element in left_half
        else:
            list[k] = right_half[j]    // Assign the smaller element to the merged list
            j = j + 1                   // Move to the next element in right_half
        k = k + 1                       // Move to the next position in the merged list

    // Add remaining elements from left_half (if any)
    while i < length of left_half:
        list[k] = left_half[i]         // Copy remaining elements to the merged list
        i = i + 1                       // Move to the next element
        k = k + 1                       // Move to the next position in the merged list

    // Add remaining elements from right_half (if any)
    while j < length of right_half:
        list[k] = right_half[j]        // Copy remaining elements to the merged list
        j = j + 1                       // Move to the next element
        k = k + 1                       // Move to the next position in the merged list
```

## Example

Consider the array `[64, 25, 12, 22, 11]`:

1. **Initial Array**:
   - The array is `[64, 25, 12, 22, 11]`.

2. **First Split**:
   - Split the array into two halves: `[64, 25]` and `[12, 22, 11]`.

3. **Second Split (Left Half)**:
   - Split `[64, 25]` into `[64]` and `[25]`.

4. **Merge Left Half**:
   - Merge `[64]` and `[25]`:
     - Compare 64 and 25.
     - Resulting array after merge: `[25, 64]`.

5. **Second Split (Right Half)**:
   - Split `[12, 22, 11]` into `[12]` and `[22, 11]`.

6. **Third Split (Right Half)**:
   - Split `[22, 11]` into `[22]` and `[11]`.

7. **Merge Right Half**:
   - Merge `[22]` and `[11]`:
     - Compare 22 and 11.
     - Resulting array after merge: `[11, 22]`.

8. **Merge Right Half**:
   - Merge `[12]` and `[11, 22]`:
     - Compare 12 and 11.
     - Resulting array after merge: `[11, 12, 22]`.

9. **Final Merge**:
   - Merge the two sorted halves `[25, 64]` and `[11, 12, 22]`:
     - Compare 25 and 11.
     - Resulting array after merge: `[11, 12, 22, 25, 64]`.

The final sorted array is `[11, 12, 22, 25, 64]`.


## Complexity Analysis

- **Time Complexity**: 
  - Best Case: O(n log n)
  - Average Case: O(n log n)
  - Worst Case: O(n log n)
  
- **Space Complexity**: O(n) due to the temporary arrays used for merging.

## Conclusion

Merge sort is a reliable and efficient sorting algorithm ideal for large datasets. Its stable sorting and predictable time complexity make it a popular choice in various applications.
