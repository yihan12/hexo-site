---
title: https的图片在移动端展示问题
date:
tags: [Bug, 兼容性]
categories: [Bug, 兼容性, img]
---

### 问题描述

引入的 src 图片地址是 https 时，在 pc 端和 h5 均正常显示，但在手机端均无法显示，并且图片链接在微信里面也无法打开；

### 解决方案

```html
<meta name="referrer" content="never" />

// 或

<img
  src="https://example.com/images/myimage.jpg"
  alt="Some image"
  referrerpolicy="no-referrer"
/>
```

```
当网站使用refresh字段进行跳转的时候，大多数浏览器不发送referer;

从用户从一个HTTPS的网站点击链接到另一个HTTP的网站时，不发送referer;

html5中，a标签的rel = “noreferrer”, 可以让浏览器不发送referer;

使用Data URI scheme链接的，浏览器也不发送referer;

使用Content Security Policy, 也可以让浏览器不发送referer;

在html头部中使用meta标签来控制不让浏览器发送referer;

用户手输入网址或是从收藏夹、书签中访问。
```

```
never

always

origin

default
```

1.如果 referer-policy 的值为 never：删除 http head 中的 referer；

2.如果 referer-policy 的值为 default：如果当前页面使用的是 https 协议，而正要加载的资源使用的是普通的 http 协议，则将 http header 中的 referer 置为空；

3.如果 referer-policy 的值为 origin：只发送 origin 部分；

4.如果 referer-policy 的值为 always：不改变 http header 中的 referer 的值，注意：这种情况下，如果当前页面使用了 https 协议，而要加载的资源使用的是 http 协议，加载资源的请求头中也会携带 referer。
