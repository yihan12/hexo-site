---
title: ES6模块和CommonJS的异同
date:
tags: [JavaScript, JavaScript面试]
categories: [前端, JavaScript, ES6模块和CommonJS的异同]
---

# 相同点

- 对引入对象进行赋值，即对对象内部属性的值的改变

# 区别

- commonJS 模块运行时加载，ES6 模块是输出编译时输出接口
- commonJS 模块 require 同步加载模块，ES6 import 是异步的
- commonJS 模块 require 对模块的浅拷贝，ES6 import 是对模块的引入，只存只读不改变其值 指针指向不能变类似 const
- import 接口 read-only 不能改变变量值，
