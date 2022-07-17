---
tags: app/obsidian
alias: Admonition 
---

**简介：**
文本框渲染

**使用方法：**
在代码块中填入 `title:` 来更改默认的渲染的标题；
在代码块中填入 `collapse:` 来更改默认的渲染的折叠情况；
在代码块中填入 `icon:` 来更改默认的渲染的图标；
在代码块中填入 `color:` 来更改默认的渲染的颜色；

**实例：**
代码块：
`````ad-note
title: Nested Admonitions
collapse: open

Hello!

````ad-note
title: This admonition is nested.
This is a nested admonition!

```ad-warning
title: This admonition is closed.
collapse: close
```

````

This is in the original admonition.
`````
引用：
> [!quote: This is the title!] > This is an admonition!、

**相关：**
* Obsidian 插件之 Admonition - AllinBon的文章 - 知乎 https://zhuanlan.zhihu.com/p/391252867
* [[-【Obsidian-插件】Obsidian插件MOC]]