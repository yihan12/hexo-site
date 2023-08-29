---
title: 插入排序
date:
tags: [leetcode, 插入排序]
categories: [前端, leetcode, 插入排序]
---

### 逻辑

- 1、序列的第一个元素看成一个有序序列，第二个元素到序列末尾看成未排序序列；
- 2、取未排序序列的第一个元素与有序序列进行比较，并插到有序序列合适的位置；
- 3、重复步骤 2，直至未排序序列末尾为止。

### JavaScript 代码实现

```javascript
const arr = [1, 2, 6, 34, 7, 9, 11, 16, 13, 19, 0, 3]
function insertionSort(arr) {
  let len = arr.length
  for (let i = 1, max = len; i < max; i++) {
    let currentI = arr[i]
    let j = i - 1
    // 把当前的元素与已排序列进行比较（从最后一位开始），如果已排序列元素大于当前元素，就把已排序列的元素向后移动一位，依次类推。
    while (j >= 0 && arr[j] > currentI) {
      arr[j + 1] = arr[j]
      j--
    }
    arr[j + 1] = currentI
  }
  return arr
}
console.log(insertionSort(arr)) // [0, 1, 2, 3, 6, 7, 9, 11, 13, 16, 19, 34]
```
