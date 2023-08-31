---
title: 选择排序
date:
tags: [leetcode, 选择排序]
categories: [前端, leetcode, 选择排序]
---

### 逻辑

- 1、在序列 arr 中找到最大（Max）或者最小（Min）的值，并将该值存在排序序列的起始位置。
- 2、再从剩下的原序列 arr 中找到最大（Max）或者最小（Min）的值，并将该值存在排序序列的末尾。
- 3、重复步骤 2 的操作。

### JavaScript 代码实现

```javascript
const arr = [1, 2, 6, 34, 7, 9, 11, 16, 13, 19, 0, 3]
function selectionMaxSort(arr) {
  let len = arr.length
  for (let i = 0, max = len - 1; i < max; i++) {
    let MaxIndex = i
    for (let j = i + 1, max = len; j < max; j++) {
      if (arr[MaxIndex] < arr[j]) {
        MaxIndex = j
      }
    }
    let temp = arr[i]
    arr[i] = arr[MaxIndex]
    arr[MaxIndex] = temp
  }
  return arr
}
function selectionMinSort(arr) {
  let len = arr.length
  for (let i = 0, max = len - 1; i < max; i++) {
    let MinIndex = i
    for (let j = i + 1, max = len; j < max; j++) {
      if (arr[MinIndex] > arr[j]) {
        MinIndex = j
      }
    }
    let temp = arr[i]
    arr[i] = arr[MinIndex]
    arr[MinIndex] = temp
  }
  return arr
}
console.log(selectionMaxSort(arr)) // [34, 19, 16, 13, 11, 9, 7, 6, 3, 2, 1, 0]
console.log(selectionMinSort(arr)) // [0, 1, 2, 3, 6, 7, 9, 11, 13, 16, 19, 34]
```
