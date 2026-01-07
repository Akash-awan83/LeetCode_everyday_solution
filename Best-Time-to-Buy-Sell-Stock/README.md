#  LeetCode 121: Best Time to Buy and Sell Stock (Summary)

## **Problem at a Glance**
The goal is to find the maximum profit from buying a stock on one day and selling it on a future day. If no profit is possible, return `0`.



## **Summary of Approaches**

I implemented this problem using three distinct methods to analyze performance and efficiency:

### **1. Brute Force Approach**
- **Method:** Uses two nested loops to check every possible buy/sell pair.
- **Complexity:** $O(n^2)$ Time | $O(1)$ Space.
- **Outcome:** **Inefficient.** Resulted in *Time Limit Exceeded (TLE)* for large inputs ($10^5$).

### **2. Two Pointers (Sliding Window)**
- **Method:** Uses `Left` (Buy) and `Right` (Sell) pointers. If a lower price is found, the `Left` pointer jumps to `Right`.
- **Complexity:** $O(n)$ Time | $O(1)$ Space.
- **Outcome:** **Fast.** Efficiently handles large arrays in a single pass.

### **3. Optimal One-Pass (Greedy)**
- **Method:** Tracks the `min_price` seen so far and updates `max_profit` at each step.
- **Complexity:** $O(n)$ Time | $O(1)$ Space.
- **Outcome:** **Best/Cleanest.** This is the industry-standard solution for this problem.


## **Efficiency Comparison**

| Approach | Time Complexity | Space Complexity | Status |
| :--- | :--- | :--- | :--- |
| **Brute Force** | $O(n^2)$ | $O(1)$ |  Failed (TLE) |
| **Two Pointers** | $O(n)$ | $O(1)$ |  Passed |
| **Optimal One-Pass** | **$O(n)$** | **$O(1)$** |  **Winner** |





## ** Key Learning**
- Nested loops ($O(n^2)$) are not suitable for constraints like $10^5$.
- Single-pass algorithms ($O(n)$) are essential for processing large-scale financial data.
- Tracking a minimum value while iterating (Greedy approach) simplifies complex problems significantly.

