# squares-of-a-sorted-array
Link: https://leetcode.com/problems/squares-of-a-sorted-array/

## Code
```python
class Solution:
    def sortedSquares(self, nums: List[int]) -> List[int]:
        # i = 1
        # while i<len(nums):
        #     nums[i-1] = nums[i-1] * nums[i-1]
        #     sq = nums[i] * nums[i]
        #     prevSq = nums[i-1] * nums[i-1]
        #     if prevSq > sq:
        #         tmp = nums[i-1]
        #         nums[i-1] = nums[i]
        #         nums[i] = tmp
        #     i=i+1
        # return nums
        for i in range(0,len(nums)):
            nums[i] *= nums[i]
        nums.sort() 
        return nums
```

- 
- 다른 접근법으로 풀어봐야 할듯.