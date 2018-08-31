---
title: leetcode-1.两数之和(Two Sum)
date: 2018-06-13 07:11:50
tags: leetcode
categories: leetcode
---
## 题目描述

给定一个整数数组和一个目标值，找出数组中和为目标值的两个数。

你可以假设每个输入只对应一种答案，且同样的元素不能被重复利用。
<!-- more -->

## 示例

```
给定 nums = [2, 7, 11, 15], target = 9

因为 nums[0] + nums[1] = 2 + 7 = 9
所以返回 [0, 1]
```

## 方法1
遍历2遍数组，从第0个元素开始，依次尝试其后面的元素与之相加有无满足目标值的情况。

### 尝试代码(Python3)
```bash
class Solution:
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
	# 方法一 遍历两次数组
        l = len(nums)
        for i in range(l-1):
            for j in range(i+1,l):
                if nums[i] + nums[j] == target:
                    return i,j


if __name__ == "__main__":
    n = [3, 2, 4, 11, 15]
    t = 6
    s = Solution()
    print(s.twoSum(n, t))
                
```
我们先自己在本地运行一下，运行结果没问题之后，提交到leetcode。
注意：只需要提交Solution部分就行。
果不其然，这种遍历两次数组的土办法真的是太慢了。leetcode返回的结果为：执行20个测试用例花了7276ms。
真的是太慢了--!
于是我们又有了第二种想法……

## 方法2
可不可以只遍历一次数组呢？
用目标值减去当前元素，然后找出得到的值在数组中的位置。
### 尝试代码(Python3)
```bash
class Solution:
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        # 方法二 遍历一次数组
        l = range(len(nums))
        for i in l:
            temp = target - nums[i]
            if temp in nums and nums.index(temp) != i:
                return i, nums.index(temp)


if __name__ == "__main__":
    n = [3, 2, 4, 11, 15]
    t = 6
    s = Solution()
    print(s.twoSum(n, t))
```
这次的运行结果比上次好一点点，用了1400ms,好像还是有点慢儿
难道我们要排序？不行！太费脑子了！
看了排名较靠前的解决方法，真的是清清爽爽！请看方法三
## 方法3
字典，类似方法二，用目标值减去数组元素得到结果，将结果与数组元素的位置存入字典中。
若有结果在字典中，则会满足 字典中结果 + 当前数组元素 = 目标值，返回字典中结果产生时对应数组元素的位置与当前数组元素的位置。
好像有点绕？emmm...好好消化一下
### 尝试代码(Python3)

```bash
class Solution:
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
	# 方法三 使用字典
        d = {}
        for i, num in enumerate(nums):
            print(i,num)
            if target - num in d:
                return [d[target - num], i]
            d[num] = i


if __name__ == "__main__":
    n = [3, 2, 4, 11, 15]
    t = 6
    s = Solution()
    print(s.twoSum(n, t))
```
本地测试没啥问题，提交！
40ms！！！
从7000ms提高到了40ms，虽然每次提交返回的时间稍有不同，但是，用了字典以后真的是快了不少。
关于字典的详细内容可以到一起学Python分类中查看（可能还没更新到那儿）。
以上。


