# Kadane's Algorithm

Suppose you want to find the largest contiguous subarray sum of an array of positive numbers. For example, given the list of numbers `[-2,1,-3,4,-1,2,1,-5,4]`, you want a way to determine that the contiguous subarray `[4,-1,2,1]` has the largest sum.

The intuition comes from the fact that the largest sum at any point `i` is the maximum of the largest sum at `i - 1` and `i`. We can use dynamic programming to take advantage of this.

## [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)

Given an integer array nums, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

```python3
def maxSubArray(self, nums: List[int]) -> int:
  if len(nums) == 0:
    return 0

  max_so_far = nums[0]

  for i in range(1, len(nums)):
    nums[i] = max(nums[i - 1] + nums[i], nums[i])
    max_so_far = max(max_so_far, nums[i])

  return max_so_far
```
