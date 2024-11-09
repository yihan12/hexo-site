---
title: 输入url,到页面展示的过程
date:
tags: [JavaScript, JavaScript面试]
categories: [前端, JavaScript, 输入url, 到页面展示的过程]
---

# 过程

- 输入 url
- 浏览器缓存 - 系统缓存 - 路由器缓存 有缓存显示页面内容，没有就往下执行
- http 请求前 DNS 解析 ip 地址
- tcp 连接 三次握手 浏览器发送 http 请求 请求数据包
- 服务器收到请求，返回数据到浏览器
- http 响应
- 读取页面内容 渲染 解析代码
- 生成 DOM 树，解析 css 样式，js 交互，渲染显示页面
