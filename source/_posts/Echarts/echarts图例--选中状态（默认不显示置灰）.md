---
title: 【Echarts使用】之 图例选中状态
date:
tags: [前端, Echarts]
categories: [前端, Echarts, legend]
---

图例选中状态表。

```
legend:{
    selected: {
        // 选中'系列1'
        '系列1': true,
        // 不选中'系列2'
        '系列2': false
    }
}
```

使用

```
legend: {
    show: true,
    selected: {
      '1星': true, '2星': true, '3星': true, '4星': false, '5星': false
    },
    bottom: 0
},
```
