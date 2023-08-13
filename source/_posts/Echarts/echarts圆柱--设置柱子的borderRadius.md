---
title: 【Echarts使用】之 设置柱子borderRadius
date:
tags: [前端, Echarts]
categories: [前端, Echarts, borderRadius]
---

```
series:[
    {
        type: 'bar',
        stack: 'Total',
        itemStyle: {
            borderColor: bgColor,
            borderRadius: [4, 4, 4, 4], // 圆柱
            color: bgColor
        },
        emphasis: {
            itemStyle: {
                borderColor: bgColor,
                color: bgColor
            }
        },
    }
]
```
