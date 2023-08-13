---
title: 【Echarts使用】之 无拐点
date:
tags: [前端, Echarts]
categories: [前端, Echarts, symbolSize]
---

### 无拐点

```
series: [
    {
      data: [820, 932, 901, 934, 1290, 1330, 1320],
      type: 'line',
      smooth: true, //关键点，为true是不支持虚线的，实线就用true
      symbolSize:0,   // 折线拐点圆的大小

    }
]
```

### 折线线型

```
series: [
    {
      data: [820, 932, 901, 934, 1290, 1330, 1320],
      type: 'line',
      lineStyle:{

                  width:2,
                  type:'dotted'  //'dotted'虚线 'solid'实线 'dashed'虚线


      }
    }
]

```
