---
title: 动态规划的基础
date:
tags: [算法, 动态规划]
categories: [前端, 算法, 动态规划]
---

# 基本性质

- 和分治相似
  - 动态规划也是将原问题分解成子问题求解
- 和分治不同
  - 不是通过分治的递归方式，而是自底向上的求解问题

# 机器人问题

## 分治

```
path(i,j) = {
  0,                              i=0,j=0;
  1,                              i=0,j不等于0 或者i不等于0，j=0;
  path(i-1,j)+path(i,j-1),        其他
}
```

# 动态规划适应场景

1. 子问题并不独立，即子问题是可能重复的
2. 主要用于优化问题（求最优解），且问题具有最优子结构性质

## 最优子结构性质

> 最优子结构性质指原问题的最优解一定包含了子问题的最优解

最短路径问题，具有最优子结构性质

# 基本步骤

1. 定义子问题，并分析最优解的结构特征

- 分治通常是将原问题对半分，而动态规划是将 n 规模问题分解成 n-1 规模问题

2. 找出最优解对应的最优值，并递归定义最优值
3. 以自底而上的方式计算出最优值
4. 根据计算最优值时得到的信息，构造最优解
