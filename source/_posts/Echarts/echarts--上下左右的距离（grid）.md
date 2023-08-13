---
title: 【Echarts使用】之 grid
date:
tags: [前端, Echarts]
categories: [前端, Echarts, grid]
---

### 示例

```
grid: {
    top: '3%',
    left: '12%',
    right: '0%',
    bottom: '3%',
    containLabel: true
},
```

echarts 组件离容器左侧的距离。

> `containLabel`:
> containLabel 为 false 的时候：  
> grid.left grid.right grid.top grid.bottom grid.width grid.height 决定的是由坐标轴形成的矩形的尺寸和位置。
> 这比较适用于多个 grid 进行对齐的场景，因为往往多个 grid 对齐的时候，是依据坐标轴来对齐的。
>
> containLabel 为 true 的时候：  
> grid.left grid.right grid.top grid.bottom grid.width grid.height 决定的是包括了坐标轴标签在内的所有内容所形成的矩形的位置。
> 这常用于『防止标签溢出』的场景，标签溢出指的是，标签长度动态变化时，可能会溢出容器或者覆盖其他组件。
