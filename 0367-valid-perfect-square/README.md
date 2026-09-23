# [367. Valid Perfect Square](https://leetcode.com/problems/valid-perfect-square/)

**Difficulty:** Easy
**Topics:** Math, Binary Search

## Problem Statement

Given a positive integer `num`, return `true` if `num` is a perfect square or `false` otherwise.

A perfect square is an integer that is the square of an integer. In other words, it is the product of some integer with itself.

**Note:** You must not use any built-in library function, such as `sqrt`.

### Example 1:
```
Input: num = 16
Output: true
Explanation: We return true because 4 * 4 = 16 and 4 is an integer.
```

### Example 2:
```
Input: num = 14
Output: false
Explanation: We return false because 3.742 * 3.742 = 14 and 3.742 is not an integer.
```

### Constraints:
* `1 <= num <= 2^31 - 1`

## Solution Approach

The solution relies on the mathematical property that every perfect square is the sum of consecutive odd numbers starting from 1. 
For example:
* `1 = 1`
* `4 = 1 + 3`
* `9 = 1 + 3 + 5`
* `16 = 1 + 3 + 5 + 7`

The code repeatedly subtracts consecutive odd numbers from `num`. If `num` eventually reaches exactly `0`, then it is a perfect square. Otherwise, if it becomes less than `0`, it is not.
