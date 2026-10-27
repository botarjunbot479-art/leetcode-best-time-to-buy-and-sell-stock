# LeetCode: Best Time to Buy and Sell Stock

- slug: `best-time-to-buy-and-sell-stock`
- id: 121
- difficulty: Easy
- tags: Array, Dynamic Programming
- url: https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
- status: **solved_verified**
- detail: Local verified 2/2
- source: LeetCode public GraphQL (no login)
- learned_at: 2026-10-27T09:23:11.494676+00:00

## Problem
You are given an array prices where prices[i] is the price of a given stock on the ith day.

You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.

Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

 

Example 1:

Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.

Example 2:

Input: prices = [7,6,4,3,1]
Output: 0
Explanation: In this case, no transactions are done and the max profit = 0.

 

Constraints:

	- 1 5
	- 0 4

## Example testcases (from LeetCode)
```
[7,1,5,3,6,4]
[7,6,4,3,1]
```

## Solution (local)
```python
def max_profit(prices):
    best = 0
    low = float("inf")
    for p in prices:
        low = min(low, p)
        best = max(best, p - low)
    return best

```
