# LeetCode 164 - Maximum Gap

## Problem

Given an integer array `nums`, return the maximum difference between two successive elements after sorting the array.

If the array contains less than two elements, return `0`.

The goal is to find the largest gap between consecutive numbers in the sorted array.

---

## Example 1

**Input:**

```text
nums = [3,6,9,1]
```

**Output:**

```text
3
```

**Explanation:**

After sorting:

```text
[1,3,6,9]
```

The gaps are:

```text
3 - 1 = 2
6 - 3 = 3
9 - 6 = 3
```

The maximum gap is:

```text
3
```

---

## Example 2

**Input:**

```text
nums = [10]
```

**Output:**

```text
0
```

**Explanation:**

There is only one element, so there are no two successive elements.

Therefore, the answer is `0`.

---

## Approach

The simple approach is to first sort the array.

After sorting, all consecutive elements are arranged in increasing order. We can then compare every pair of neighboring elements and find the largest difference.

For example:

```text
nums = [3,6,9,1]
```

After sorting:

```text
[1,3,6,9]
```

Now calculate each gap:

```text
3 - 1 = 2
6 - 3 = 3
9 - 6 = 3
```

The largest gap is `3`.

---

## Algorithm

1. Check if the array has fewer than two elements.
2. If yes, return `0`.
3. Sort the array.
4. Initialize `max_gap = 0`.
5. Traverse the sorted array from the second element.
6. Calculate the difference between the current element and the previous element.
7. Update `max_gap` if the current difference is larger.
8. Return `max_gap`.

---

## Example Walkthrough

For:

```text
nums = [3,6,9,1]
```

### Step 1: Sort the array

```text
[1,3,6,9]
```

### Step 2: Compare consecutive elements

First gap:

```text
3 - 1 = 2
```

Current maximum:

```text
max_gap = 2
```

Second gap:

```text
6 - 3 = 3
```

Update:

```text
max_gap = 3
```

Third gap:

```text
9 - 6 = 3
```

The maximum remains:

```text
max_gap = 3
```

### Final Answer

```text
3
```

---

## Time Complexity

**O(n log n)**

The main operation is sorting the array, which takes `O(n log n)` time.

The second traversal takes `O(n)` time.

Therefore, the overall complexity is:

```text
O(n log n)
```

---

## Space Complexity

**O(log n)** auxiliary space for the sorting operation in Python, depending on the sorting implementation.

The algorithm itself uses only **O(1)** additional variables apart from the sorting operation.

---

## Key Concepts

* Arrays
* Sorting
* Consecutive elements
* Difference calculation
* Maximum value tracking

---

## Important Edge Cases

### One element

```text
nums = [5]
```

Output:

```text
0
```

### Two elements

```text
nums = [1,10]
```

Output:

```text
9
```

### Unsorted array

```text
nums = [3,6,9,1]
```

After sorting:

```text
[1,3,6,9]
```

Maximum gap:

```text
3
```

---

## Note

The original LeetCode problem has an important follow-up: solve the problem in **linear time without using sorting**.

This implementation uses sorting, so it provides the straightforward solution with **O(n log n)** time.

The linear-time solution can be implemented using a **bucket-based approach**, which is a more advanced technique.

---

## What I Learned

This problem helped me practice finding differences between consecutive elements after sorting.

The key idea is simple: once the numbers are sorted, the maximum gap can only occur between neighboring elements.

I also learned that there can be a difference between a straightforward solution and an optimized solution. Sorting gives an easy `O(n log n)` solution, while the follow-up requires a more advanced bucket approach to achieve `O(n)` time.

---

## LeetCode Details

* **Problem Number:** 164
* **Problem Name:** Maximum Gap
* **Difficulty:** Medium
* **Topics:** Array, Sorting, Bucket Sort
* **Language:** Python

---

## Author

T.Nandhini
