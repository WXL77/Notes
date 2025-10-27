## [两数之和](https://leetcode.cn/problems/two-sum/description/?envType=study-plan-v2&envId=top-100-liked)
1. **双指针+排序**
```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        ##返回数组中的值和索引（值，索引）
        indexed_nums = [(num, idx) for idx, num in enumerate(nums)]
        ##根据indexed_nums每个元组的第一个元素的大小升序排列
        indexed_nums.sort(key=lambda x: x[0])
        left, right = 0, len(indexed_nums) - 1
        while left < right:
            current_sum = indexed_nums[left][0] + indexed_nums[right][0]
            if current_sum == target:
                return [indexed_nums[left][1], indexed_nums[right][1]]
            elif current_sum < target:
                left += 1
            else:
                right -= 1
        return []
```
2.  **哈希表**
```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        ##创建空哈希表（字典），hashtable={数值: 原始索引}，hashtable[2] = 0 含义：数值2出现在索引0位置
        hashtable = {}
        for i, num in enumerate(nums):
            if target - num in hashtable:
                return [hashtable[target - num], i]
            hashtable[nums[i]] = i
        return []
```
