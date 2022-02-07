# rotate-array
Link: https://leetcode.com/problems/rotate-array/

## Code
```python
        """
        Do not return anything, modify nums in-place instead.
        """
          # for kk in range(k):
        #     end = len(nums)
        #     endNum = nums[end-1]
        #     for i in range(end-1,0,-1):
        #         nums[i] = nums[i-1]
        #     nums[0] = endNum
        #     #print(nums)

        # newNums = nums
        # newNums[1:] = nums[0:len(nums)-2]
        # nums0 = nums[0]
        # # newNums[0] = nums[len(nums)-1]
        # print(nums,newNums)
        # nums = newNums

        newNums = [0]
        newNums[0:k] = nums[-k:]
        #print(newNums, nums)
        newNums[k:] = nums[0:-k]
        #print(newNums,nums)
        nums = newNums
```

- 마지막 접근법이 뭐가 잘못된건지 모르겠는데(아마 문제가 의도한 솔루션도 아닐듯)리트코드 안에선 답을 안받아준다... 
	- 노트북 로컬에서 파이썬 콘솔로 돌려보면 잘 나오는데... 이상함. 
	- 질문 글 올려봄. https://leetcode.com/problems/rotate-array/discuss/1751900/189-rotate-array-getting-the-correct-answer-but-leetcode-wouldnt-accept