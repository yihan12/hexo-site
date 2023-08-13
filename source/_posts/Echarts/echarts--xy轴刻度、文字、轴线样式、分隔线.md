---
title: 【Echarts使用】之 x/y轴刻度、文字、轴线样式、分割线
date:
tags: [前端, Echarts]
categories: [前端, Echarts, xAxis]
---

### 隐藏 x/y 轴刻度

```
// x轴
xAxis: {
    type: 'category',
    splitLine: { show: false },
    data: ['11/25', '11/26', '11/27', '11/28', '11/29', '11/30', '12/1'],
    axisTick: {
        show: false //隐藏x轴刻度
    },
},
// y轴
yAxis: {
    type: 'category',
    splitLine: { show: false },
    data: ['11/25', '11/26', '11/27', '11/28', '11/29', '11/30', '12/1'],
    axisTick: {
        show: false //隐藏y轴刻度
    },
},
```

### 更改 x/y 轴文字

```
//x轴
xAxis: {
    type: 'category',
    // offset: 40,
    splitLine: { show: false },
    data: [],
    axisLabel: {
        show: true,
        textStyle: {
            color: '#6B6E7F',  //更改坐标轴文字颜色
            fontSize: 9      //更改坐标轴文字大小
        }
    }
},
//y轴
yAxis: {
    type: 'category',
    // offset: 40,
    splitLine: { show: false },
    data: [],
    axisLabel: {
        show: true,
        textStyle: {
            color: '#6B6E7F',  //更改坐标轴文字颜色
            fontSize: 9      //更改坐标轴文字大小
        }
    }
},
```

### 更改 x/y 轴线样式

```
// x轴
xAxis: {
    type: 'category',
    // offset: 40,
    splitLine: { show: false },
    data: [],
    axisLine: {
        show: false,
        lineStyle: {
            type: 'dashed',
            color: '#86899D'
        }
    } //0 轴线设置样式
},
// y轴
yAxis: {
    type: 'category',
    // offset: 40,
    splitLine: { show: false },
    data: [],
    axisLine: {
        show: false,
        lineStyle: {
            type: 'dashed',
            color: '#86899D'
        }
    } //0 轴线设置样式
},
```

### x/y 轴分隔线

```
// x轴
xAxis: {
    type: 'value',
    axisLabel: {
        show: false,
        interval: 'auto',
        formatter: '{value} AM'
    },
    axisTick: {
        show: false
    },
    splitLine: {
        show: false,
        lineStyle: {
            type: 'dashed',
            color: '#86899D'
        }
    } //设置y轴分割线样式
},
// y轴
yAxis: {
    type: 'value',
    axisLabel: {
        show: false,
        interval: 'auto',
        formatter: '{value} AM'
    },
    min: 20,
    max: 33, // y轴的展示范围
    axisTick: {
        show: false
    },
    splitLine: {
        show: false,
        lineStyle: {
            type: 'dashed',
            color: '#86899D'
        }
    } //设置y轴分割线样式
},
```
