---
title: 希尔排序
date:
tags: [leetcode, 希尔排序]
categories: [前端, leetcode, 希尔排序]
---

### 基本思想

> 将整个待排序序列进行的记录分割成若干个子序列，进行直接插入排序；待整个序列基本有序时，再对整个序列进行直接插入排序。

### 逻辑

- 1、选择一个增量序列 t1,t2....tk,其中 ti>tj，tk=1；
- 2、按增量序列个数 k,对序列进行 K 趟排序；
- 3、每趟排序，根据对应的增量 ti，将待排序列分割成若干长度为 m 的子序列，分别对各子表进行直接插入排序。仅增量因子为 1 时，整个序列作为一个表来处理，表长度即为整个序列的长度。

### JavaScript 代码实现

```javascript
const arr = [1, 9, 7, 10, 5, 8, 11, 14, 66, 0]
function shellSort(arr) {
  let len = arr.length
  for (let gap = Math.floor(len / 2); gap > 0; gap = Math.floor(gap / 2)) {
    for (let i = gap; i < len; i++) {
      let j = i
      let current = arr[i]
      while (j - gap >= 0 && current < arr[j - gap]) {
        arr[j] = arr[j - gap]
        j = j - gap
      }
      arr[j] = current
    }
  }
  return arr
}
function shellSort2(arr) {
  let len = arr.length,
    temp,
    gap = 1
  while (gap < len / 3) {
    gap = gap * 3 + 1
  }
  for (gap; gap > 0; gap = Math.floor(gap / 3)) {
    for (let i = gap; i < len; i++) {
      temp = arr[i]
      let j = i - gap
      for (j; j >= 0 && arr[j] > temp; j -= gap) {
        arr[j + gap] = arr[j]
      }
      arr[j + gap] = temp
    }
  }
  return arr
}
console.log(shellSort(arr)) // [0, 1, 5, 7, 8, 9, 10, 11, 14, 66]
console.log(shellSort2(arr)) // [0, 1, 5, 7, 8, 9, 10, 11, 14, 66]
```
