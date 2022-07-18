---
alias: YAML
---

# 简介
正如YAML所表示的YAML Ain’t Markup Language，YAML 是一种简洁的非标记语言。YAML以数据为中心，使用空白，缩进，分行组织数据，从而使得表示更加简洁易读。

由于实现简单，解析成本很低，YAML特别适合在脚本语言中使用。列一下现有的语言实现：Ruby，Java，Perl，Python，PHP，JavaScript等。


# 实例
## 实例1
title: 实际文件名，因为我的文件名可能会是数字串  
date: 建立日期  
tags:  
\- 标签1  
alias: 别名1  
category: 类别  
stars: 星级（可选，当为评测笔记的时候会存在）  
from: 基于什么，来自什么  
url: 文章链接（如果已经发文或者已经存在在 Obsidian publish 上的话）

## 实例2
created: 2021-10-13 09:24
modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
category: 鹦鹉
name: 小灰灰
aliases: xiaohuihui, little gray
gender: 男
birthday: 2020-05-19
tags: parrot cockatiel bird



# 相关内容
[[Obs＃57] Obsidian YAML区tags标签自动补全的3种方法_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Qv411u7HC?vd_source=f2038330b5d9967a70e2be6f24dbeed5)
[Obsidian学习笔记分享 - 哔哩哔哩](https://www.bilibili.com/read/cv15307070/)
[obsidian使用教程_srmmh的博客-CSDN博客_obsidian使用方法](https://blog.csdn.net/u013074761/article/details/114624523)
[Obsidian 的 YAML Front matter 介绍 - 知乎](https://zhuanlan.zhihu.com/p/370113792)
[为 obsidian 中的文件批量添加 front matter - 简书](https://www.jianshu.com/p/317fa053861b)

