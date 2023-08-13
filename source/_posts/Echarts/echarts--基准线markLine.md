---
title: 【Echarts使用】之基准线markLine
date:
tags: [前端, Echarts]
categories: [前端, Echarts, markLine]
---

### 设置了两条基准线

```
markLine: {
    symbol: "none",
    data: [{
        label: {
            width: "30",
            position: 'start',
            formatter: t('sleepManage_cycle.sameChart.rs'),
            fontSize: '10',
            color: '#86899D',
            overflow: 'break',
        },
        silent: false,
        lineStyle: {
            type: "dashed",
            color: "#714EB3"
        },
        yAxis: 10
    },
    {
        label: {
            width: "30",
            position: 'start',
            formatter: t('sleepManage_cycle.sameChart.qc'),
            fontSize: '10',
            color: '#86899D',
            overflow: 'break',
        },
        silent: false,
        lineStyle: {
            type: "dashed",
            color: "#3F6293"
        },
        yAxis: 1
    }]
},
```

### 关键参数

> `yAxis`:基准线的坐标

> `overflow`:  
> 'truncate' 截断，并在末尾显示 ellipsis 配置的文本，默认为...  
> 'break' 换行  
> 'breakAll' 换行，跟'break'不同的是，在英语等拉丁文中，'breakAll'还会强制单词内换行

> `ellipsis`:在 overflow 配置为'truncate'的时候，可以通过该属性配置末尾显示的文本。
