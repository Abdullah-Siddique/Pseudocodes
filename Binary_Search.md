# Binary Search

Binary search refers to finding an element (any element you wish) in a sorted array. The process involves the following steps:

1. Look at the middle of the sorted list.
2. If the item you're searching for is smaller than middle, look in the left half.
3. If it's bigger, look in the right half.
4. Repeat until you find it.

## Pseudocode

```
while left <= right:
  middle = (left + right) // 2
  if array[middle] == target:
    return middle
  else if target < array[middle]:
    right = middle - 1
  else:
    left = middle + 1
return -1
```
