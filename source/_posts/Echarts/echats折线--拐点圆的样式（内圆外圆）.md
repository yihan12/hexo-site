---
title: 【Echarts使用】之 拐点圆样式
date:
tags: [前端, Echarts]
categories: [前端, Echarts, symbol]
---

```
series:[
    {
        type: 'line',
        connectNulls: true,//无数据是是否连线
        stack: 'Total',
        symbol: 'circle', //拐点样式
        symbolSize: 4, //拐点圆大小
        itemStyle: {
            color: '#292B37', //拐点内圆颜色
            borderColor: '#5B5E74', //拐点外圆颜色
            width: 2, //拐点内圆大小
        },
    }
]
```
