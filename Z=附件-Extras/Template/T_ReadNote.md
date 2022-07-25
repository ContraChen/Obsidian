---
title: {{VALUE:title}}
originalName: {{VALUE:originalNameWithQuote}}
author: {{VALUE:authorWithQuote}}
transAuthor: {{VALUE:transAuthor}}
publisher: {{VALUE:publisher}}
rating: {{VALUE:rating}}
tags: book
RelatedBooks: {{VALUE:relatedBooks}}
ISBN: {{VALUE:isbn}}
type: ReadNote
link: {{VALUE:link}}
cover: {{VALUE:coverUrl}}
pages: {{VALUE:pages}}
BeginDate: {{DATE}}
publishDate: {{VALUE:publishDate}}
EndDate:
alias:
pageprogress:
banner_icon: 📖
banner: {{VALUE:coverUrl}}
status: 想读
---

现在是 `=date(now)`
距离第一次看《{{VALUE:name}}》已经过去了==`=(date(today)-this.BeginDate).days`==天
此刻有什么新[[#想法]]呢？
````ad-abstract
title: 在那段时间里阅读的其他书籍：
icon: book-open

```dataview
list "开始阅读于 "+BeginDate
from #book
where file.name!=this.file.name & file.name!="T_ReadNote" & ((((date(BeginDate)-this.BeginDate).days<=90 & (date(BeginDate)-this.BeginDate).days>=0)) | (((date(this.BeginDate)-BeginDate).days<=90 & (date(this.BeginDate)-BeginDate).days>=0)))
```
````
[[-我的书单|查看完整书单]]

---
# {{VALUE:name}}

![{{VALUE:name}}|300]({{VALUE:coverUrl}})

## 简介
### 书籍简介

{{VALUE:intro}}

### 作者简介

{{VALUE:authorIntro}}

## 原文摘录
> {{VALUE:quote1}}

> {{VALUE:quote2}}

## 想法
