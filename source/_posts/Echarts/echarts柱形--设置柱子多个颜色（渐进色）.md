---
title: 【Echarts使用】之 设置柱状图渐进式
date:
tags: [前端, Echarts]
categories: [前端, Echarts, itemStyle]
---

```
series:[
    {
        type: 'bar',
        stack: 'Total',
        itemStyle: {
            borderRadius: [4, 4, 4, 4], // 圆柱
            color: function (params) {
                //首先定义一个数组
                const colorList = [
                    {
                        x: 0,
                        y: 1,
                        x2: 0,
                        y2: 0,
                        colorStops: [{
                            offset: 0, color: '#3BABFF' // 0% 处的颜色
                        }, {
                            offset: 1, color: '#7548FF' // 100% 处的颜色
                        }],
                        global: false // 缺省为 false
                    }, "#514FA4", "#373948"];
                if (params.data.type == "达标") {
                    return colorList[0]
                } else if (params.data.type == "未达标") {
                    return colorList[1]
                } else {
                    return colorList[2]
                }
            },
        },
    }
]
```
