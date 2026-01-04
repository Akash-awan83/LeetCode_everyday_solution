# Trapping Rain Water

## Problem Description
Given an array of non-negative integers representing an elevation map where the width of each bar is 1, the task is to compute how much water it can trap after raining.

## Intuition
The amount of water that can be stored above any bar depends on the heights of the tallest bars to its left and right. The water level at any index `i` is determined by the formula:
Water at index i = min(max_left_height, max_right_height) - height[i]

---

## Solution Approaches

### 1. Brute Force Approach
In this approach, for every single bar in the array, we traverse the entire left side to find the maximum height and the entire right side to find its maximum height.
* **Time Complexity:** O(N^2)
* **Space Complexity:** O(1)

### 2. Better Approach (Prefix & Suffix Arrays)
To avoid redundant calculations of left and right maximums, we pre-calculate two arrays:
* `prefix_max`: Stores the maximum height encountered from the left up to index `i`.
* `suffix_max`: Stores the maximum height encountered from the right up to index `i`.
This allows us to find the boundaries for any bar in O(1) time after an O(N) preprocessing step.
* **Time Complexity:** O(N)
* **Space Complexity:** O(N)

### 3. Optimal Approach (Two Pointers)
This is the most efficient solution. We use two pointers, `left` and `right`, starting at both ends of the array. We maintain `left_max` and `right_max` variables. By comparing the heights at the two pointers, we can decide which side's water level is guaranteed by the current boundaries, eliminating the need for extra space.
* **Time Complexity:** O(N)
* **Space Complexity:** O(1)

---

## Complexity Summary

| Strategy | Time Complexity | Space Complexity |
| :--- | :--- | :--- |
| Brute Force | O(N^2) | O(1) |
| Prefix/Suffix Max | O(N) | O(N) |
| Two Pointers | O(N) | O(1) |

---

## Implementation Notes
The optimal Two-Pointer approach is preferred for large datasets because it provides linear time complexity while maintaining a constant space footprint. This solution is robust and handles edge cases such as empty arrays or arrays with fewer than three bars (where no water can be trapped).
