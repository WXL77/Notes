## [两数之和](https://leetcode.cn/problems/two-sum/description/?envType=study-plan-v2&envId=top-100-liked)
1. **双指针+排序**  
   先构建每个元组为（值，索引）的数组，且按照值升序排列，然后利用双指针，从最左和最右开始不断缩小，找到和=target的两个数停止。
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
2. **哈希表**
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

## [字母异位词分组](https://leetcode.cn/problems/group-anagrams/description/?envType=study-plan-v2&envId=top-100-liked)
字母异位词指的是字母出现次数完全相同，只是排列顺序不同的字符串。下面两种方法都是基于哈希表：
1. **排序法**  
   将字符串按字母排序，异位词排序后相同
   ```python
   class Solution:
       def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
           from collections import defaultdict
           groups = defaultdict(list)
           for s in strs:
               key = ''.join(sorted(s))
               groups[key].append(s)
           return list(groups.values())
   ```
2. **计数法**  
    统计每个字母出现的次数，用一个长度 26 的数组或元组表示。
    ```python
    class Solution:
        def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
            from collections import defaultdict
            groups = defaultdict(list)
            for s in strs:
                count = [0] * 26
                for char in s:
                    count[ord(char) - ord('a')] += 1
                key = tuple(count)
                groups[key].append(s)
            return list(groups.values())
    ```

## [最长连续序列](https://leetcode.cn/problems/longest-consecutive-sequence/description/?envType=study-plan-v2&envId=top-100-liked)
1. **哈希表**
   ```python
   class Solution:
      def longestConsecutive(self, nums: List[int]) -> int:
         if not nums:
            return 0
         num_set = set(nums)
         max_length = 0
         for num in num_set:
            # 只有当 num 是序列的起点时才进入内层循环
            if num - 1 not in num_set:
               current_num = num
               current_length = 1
               while current_num + 1 in num_set:
                  current_num += 1
                  current_length += 1
               max_length = max(max_length, current_length)
         return max_length
   ```
2. **直接排序**
   ```python
   class Solution:
      def longestConsecutive(self, nums: List[int]) -> int:
         if not nums:
            return 0
         nums.sort()
         max_length = 1
         current_length = 1
         for i in range(1, len(nums)):
            if nums[i] == nums[i - 1]:
               continue  # 跳过重复
            elif nums[i] == nums[i - 1] + 1:
               current_length += 1
               max_length = max(max_length, current_length)
            else:
               current_length = 1
          return max_length
   ``` 
## [移动零](https://leetcode.cn/problems/move-zeroes/description/?envType=study-plan-v2&envId=top-100-liked)
1. **普通删去0，添加0**
   ```python
   class Solution:
      def moveZeroes(self, nums: List[int]) -> None:
         zero_count = 0
         i = 0
         while i < len(nums):
            if nums[i] == 0:
               nums.pop(i)
               zero_count += 1
            else:
               i += 1
         nums.extend([0] * zero_count)
   ```
2. **原地栈**
   ```python
   class Solution:
      def moveZeroes(self, nums: List[int]) -> None:
         stack_size = 0
         for x in nums:
            if x:
               nums[stack_size] = x  # 把 x 入栈
               stack_size += 1
         for i in range(stack_size, len(nums)):
            nums[i] = 0
   ```
3. **双指针+交换元素**
   ```python
   class Solution:
      def moveZeroes(self, nums: List[int]) -> None:
         i0 = 0
         for i in range(len(nums)):
            if nums[i]:
               nums[i], nums[i0] = nums[i0], nums[i]
               i0 += 1
   ```
## [盛最多水的容器](https://leetcode.cn/problems/container-with-most-water/?envType=study-plan-v2&envId=top-100-liked)
1. **双指针**
   ```python
   class Solution:
      def maxArea(self, height: List[int]) -> int:
         left, right = 0, len(height) - 1
         max_area = 0
         while left < right:
            h = min(height[left], height[right])
            w = right - left
            area = h * w
            max_area = max(max_area, area)
            # 移动较短的线
            if height[left] < height[right]:
               left += 1
            else:
               right -= 1
         return max_area
   ```
## [三数之和](https://leetcode.cn/problems/3sum/description/?envType=study-plan-v2&envId=top-100-liked)
1. **双指针**
   ```python
   class Solution:
      def threeSum(self, nums: List[int]) -> List[List[int]]:
         if len(nums) < 3:
            return []
         nums.sort()
         result = []
         n = len(nums)
         for i in range(n - 2):
            if i > 0 and nums[i] == nums[i - 1]:
               continue
            seen = set()
            for j in range(i + 1, n):
               complement = -nums[i] - nums[j]
               if complement in seen:
                  result.append([nums[i], complement, nums[j]])
                     while j + 1 < n and nums[j] == nums[j + 1]:
                        j += 1
               seen.add(nums[j])
         return list({tuple(triplet): triplet for triplet in result}.values())
   ```
















   

