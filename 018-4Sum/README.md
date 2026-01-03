
# 018. 4Sum

## Problem Statement
Given an array `nums` of `n` integers, return an array of all the unique quadruplets `[nums[a], nums[b], nums[c], nums[d]]` such that:
- `0 <= a, b, c, d < n`
- `a, b, c, and d` are distinct.
- `nums[a] + nums[b] + nums[c] + nums[d] == target`

## Analysis of Approaches

### 1. Brute Force Approach
- **Logic:** Using four nested loops to check every possible combination of four numbers.
- **Time Complexity:** O(n^4)
- **Space Complexity:** O(1) (excluding the space for the output).
- **Drawback:** Extremely slow for larger inputs and difficult to handle unique quadruplets without extra space.

### 2. Optimized Approach (Sorting + Three Pointers with Set)
- **Logic:** Sort the array and use three nested loops, then use a Hash Set or binary search to find the fourth element.
- **Time Complexity:** O(n^3)
- **Space Complexity:** O(n) to store unique quadruplets in a set.
- **Improvement:** Faster than brute force but still uses extra memory for duplicate management.

### 3. The Gold Standard (Sorting + Two Pointers)
- **Logic:** Sort the array and use two fixed loops for the first two numbers. Then use a two-pointer approach (left and right) for the remaining two numbers. We skip duplicates at each step to ensure unique results without using a Hash Set.
- **Time Complexity:** O(n^3)
- **Space Complexity:** O(1) (ignoring the space used by the sorting algorithm).
- **Result:** Most efficient way to solve the problem with optimal time and space.

---
"The goal is not just to solve the problem, but to find the most efficient way to navigate the constraints."
