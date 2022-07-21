---
cssClasses: cards, cards-align-bottom, cards-cover,cards-9-16, table-max,cards-cols-6
banner: "![[alpine-gbdddb9210_1920.jpg]]"
---
---
笔记导航：| [[-我的影单|我的影单]] | [[- 我的书单|我的书单]] | [[时光序iframe|时光序]] | [[微信读书iframe|微信读书]] |

---
常用功能：`button-rj` `button-douban` `button-tu` `button-heian` `button-mingliang`

---
# 最近阅读
```dataview
table without id ("![](" + cover + ")") as Cover, file.link as Name, default(split(author," ")[1],author) as "Author"
from "D3=读书-Reading"  
where status = "在读"
sort file.cday asc 
```
# 最近收看
```dataview
table without id ("![](" + cover + ")") as Cover, file.link as Name, default(split(director," ")[1],director) as "director",tags as Tag,progress as Progress
from "D4=观影-Viewing"  
where status = "在看"
sort file.cday asc 
```
---
数据：[[【合集-Buttons】Buttons Set|Buttons合集]] | [[-【MOC-合集】内容MOC合集|MOC合集]] | [[-【Obsidian-资源】Obsidian参考资料合集|OB资料合集]]

---

 