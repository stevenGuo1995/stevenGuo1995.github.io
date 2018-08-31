---
title: 'leetcode-180.连续出现的数字(Consecutive Numbers) '
date: 2018-07-11 09:49:45
tags: leetcode
---

## 题目描述

编写一个 SQL 查询，查找所有至少连续出现三次的数字。

```
+----+-----+
| Id | Num |
+----+-----+
| 1  |  1  |
| 2  |  1  |
| 3  |  1  |
| 4  |  2  |
| 5  |  1  |
| 6  |  2  |
| 7  |  2  |
+----+-----+
```

例如，给定上面的 `Logs` 表， `1` 是唯一连续出现至少三次的数字。

```
+-----------------+
| ConsecutiveNums |
+-----------------+
| 1               |
+-----------------+
```

## 解题思路

### sql代码

```sql
select distinct a.num as ConsecutiveNums
from logs as a, logs as b, logs as c
where a.id = b.id + 1 and a.id = c.id + 2 and
      a.Num = b.Num and a.Num = c.Num
```

