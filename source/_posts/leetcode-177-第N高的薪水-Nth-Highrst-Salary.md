---
title: leetcode-177.第N高的薪水(Nth Highrst Salary)
date: 2018-07-11 09:10:40
tags: leetcode
---

------

## 题目描述

编写一个 SQL 查询，获取 `Employee` 表中第 *n* 高的薪水（Salary）。

<!-- more -->

```
+----+--------+
| Id | Salary |
+----+--------+
| 1  | 100    |
| 2  | 200    |
| 3  | 300    |
+----+--------+
```

例如上述 `Employee` 表，*n = 2* 时，应返回第二高的薪水 `200`。如果不存在第 *n* 高的薪水，那么查询应返回 `null`。

```
+------------------------+
| getNthHighestSalary(2) |
+------------------------+
| 200                    |
+------------------------+
```
## 解题思路

### sql代码
```sql
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT  
BEGIN  
  declare m int;  
  set m = N - 1;  
  RETURN (  
      # Write your MySQL query statement below.  
      select distinct Salary 
      from Employee
      order by Salary desc 
      limit m,1  
  );  
END  
```
### 学到的东西
limit的用法
declare
set
