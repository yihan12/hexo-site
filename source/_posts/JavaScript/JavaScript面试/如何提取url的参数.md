---
title: 如何提取url的参数
date:
tags: [JavaScript, JavaScript面试]
categories: [前端, JavaScript, 如何提取url的参数]
---

```javascript
let url = 'https://baidu.com?a=1&b=12&c=info'
let getUrlParams = function (URL) {
  let url = URL.split('?')[1]
  let urlsearchparam = new URLSearchParams(url)
  const params = Object.fromEntries(urlsearchparam.entries())
  return params
}
console.log(getUrlParams(url))
```
