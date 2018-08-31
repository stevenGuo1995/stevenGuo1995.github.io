---
title: leetcode-7.反转整数(Reverse Integer)
date: 2018-06-13 08:23:02
categories: leetcode
---
## 题目描述

给定一个 32 位有符号整数，将整数中的数字进行反转。
<!-- more -->
## 示例

示例 1: 
输入: 123
输出: 321

示例 2:
输入: -123
输出: -321

示例 3:
输入: 120
输出: 21

注意:
假设我们的环境只能存储 32 位有符号整数，其数值范围是 [−2^31,  2^31 − 1]。根据这个假设，如果反转后的整数溢出，则返回 0。
## 思路

## 关键代码(Python)
```bash
class Solution:
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        s = str(abs(x))
        r = int(s[::-1])
        if -2 ** 31 < r < 2 ** 31 - 1:
            if x >= 0:
                return r
            else:
                return -r
        else:
            return 0
```
