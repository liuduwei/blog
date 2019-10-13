---
title: leetcode_study1
date: 2019-10-13 19:21:20
tags: leetcode study
---

## leetcode刷题1：两数之和（简单）

### 解法一：暴力遍历

这个题最容易想到的解法就是暴力遍历，但是**时间复杂度**和**空间复杂度**都很高。而且有一点要注意的是：两个数不能重复，这就需要注意**python**中的列表方法*index*是返回的第一个出现的元素的索引，比如说一个列表：**[3,3,5]**那**index**方法返回的就是**0不是1**。代码如下：

```python
//暴力遍历解法
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            for j in range(i + 1 , len(nums)):
                if nums[i] + nums[j] == target
                    return [i,j]
```



需要注意的是在第二个for循环里，range函数的开头是**i+1** 是为了去重。此算法时间复杂度是O（n^2)

### 解法二：哈希查找

利用字典模拟哈希查找，代码如下：



```python
  //遍历查字典（哈希查找）
    dct = {}//注意此处词典的键是nums的值，值是nums的索引
    for value, key in enumerate(nums):
        if target - key in dct:
            return [dct[target - key], value]
        dct[key] = value//此语句放在最后，防止出现重复的情况
```

此算法的时间复杂度是O(n),大大优化了时间，此算法对比暴力遍历算法

### 总结

以后遇到要遍历查找列表的，就优先考虑字典，充分利用字典键值对的优势。