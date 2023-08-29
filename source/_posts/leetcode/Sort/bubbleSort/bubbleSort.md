---
title: 冒泡排序
date:
tags: [leetcode, 冒泡排序]
categories: [前端, leetcode, 冒泡排序]
---

# 冒泡排序

### 逻辑

- 1、比较两个相邻的元素 a、b，如果 a>b，则把 a、b 调换位置；反之，不调换位置。
- 2、从头到尾比较每一对相邻的元素，并且重复第一步的操作。操作完这步骤后，最后一位元素就是最大的元素。
- 3、针对所有元素重复以上的步骤（最后一位元素除外）。

### JavaScript 代码实现

```javascript
const arr = [1, 2, 6, 34, 7, 9, 11, 16, 13, 19, 0, 3]
function bubbleSort(arr) {
  let len = arr.length
  for (let i = 0, max = len - 1; i < max; i++) {
    for (let j = 0, max = len - 1; j < max; j++) {
      if (arr[j] > arr[j + 1]) {
        let arrMax = arr[j]
        arr[j] = arr[j + 1]
        arr[j + 1] = arrMax
      }
    }
  }
  return arr
}
console.log(bubbleSort(arr)) // [0, 1, 2, 3, 6, 7, 9, 11, 13, 16, 19, 34]
```
