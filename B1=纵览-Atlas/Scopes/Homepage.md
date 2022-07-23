---
cssClasses: cards, cards-align-bottom, cards-cover,cards-9-16, table-max,cards-cols-5,myhome
banner: "![[alpine-gbdddb9210_1920.jpg]]"
banner_x: 0.5
banner_y: 0.5
---
---
```ad-icon
<svg xmlns="http://www.w3.org/2000/svg" aria-label="Calendar" role="img" viewBox="0 0 512 512">
  <path d="M512 455c0 32-25 57-57 57H57c-32 0-57-25-57-57V128c0-31 25-57 57-57h398c32 0 57 26 57 57z" fill="#e0e7ec"></path>
  <path d="M484 0h-47c2 4 4 9 4 14a28 28 0 1 1-53-14H124c3 4 4 9 4 14A28 28 0 1 1 75 0H28C13 0 0 13 0 28v157h512V28c0-15-13-28-28-28z" fill="#cf5659"></path>
 <g fill="#f3aab9">
        <circle cx="462" cy="136" r="14"/>
        <circle cx="462" cy="94" r="14"/>
        <circle cx="419" cy="136" r="14"/>
        <circle cx="419" cy="94" r="14"/>
        <circle cx="376" cy="136" r="14"/>
        <circle cx="376" cy="94" r="14"/>
      </g>
  <text id="month" x="32" y="164" fill="#fff" font-family="-apple-system, BlinkMacSystemFont, 'Noto Sans', 'Noto Sans CJK SC', 'Microsoft YaHei', 微软雅黑, sans-serif, 'Segoe UI', Roboto, 'Helvetica Neue', Arial" font-size="122px" style="text-anchor: left"><%+ tp.date.now("MMMM").toUpperCase() %>
  </text>
  <text id="day" x="256" y="400" fill="#333" font-family="-apple-system, BlinkMacSystemFont, 'Noto Sans', 'Noto Sans CJK SC', 'Microsoft YaHei', 微软雅黑, sans-serif, 'Segoe UI', Roboto, 'Helvetica Neue', Arial" font-size="256px" style="text-anchor: middle"><%+ tp.date.now("D") %>
  </text>
  <text id="weekday" x="256" y="480" fill="#66757f" font-family="-apple-system, BlinkMacSystemFont, 'Noto Sans', 'Noto Sans CJK SC', 'Microsoft YaHei', 微软雅黑, sans-serif, 'Segoe UI', Roboto, 'Helvetica Neue', Arial" font-size="64px" style="text-anchor: middle"><%+ tp.date.now("dddd") %>
  </text>
</svg>
```
```ad-flex
<div style="float:left"><%+ tp.date.now("A好，今天是YYYY年MM月Do dddd") %>
</div> 
<div>
<iframe style="float:right; margin-top:3px" width="300" scrolling="no" height="20" frameborder="0" allowtransparency="true" src="https://i.tianqi.com?c=code&id=34&bdc=%23&icon=4&site=14"></iframe>
<!------- 黑暗模式使用下面代码
<iframe style="float:right; margin-top:3px" width="300" scrolling="no" height="20" frameborder="0" allowtransparency="true" src="https://i.tianqi.com?color=%23%FFFFFE&c=code&id=34&bdc=%23&icon=4&site=14"></iframe>
------->
<!-----指定城市后面添加城市拼音比例如 重庆天气预报：https://i.tianqi.com/?c=code&id=34&bdc=%23&icon=4&site=14&py=chongqing------>
</div>
```
**笔记导航**:    [[-我的影单|我的影单]] | [[- 我的书单|我的书单]] | [[时光序iframe|时光序]] | [[微信读书iframe|微信读书]]
**网址导航**:    [B站动态](https://t.bilibili.com/?spm_id_from=333.1007.0.0) | [程序员导航](https://cxy521.com/) | [微信公众平台](https://mp.weixin.qq.com/) | [语雀](https://www.yuque.com/dashboard) | [GitHub](https://github.com/)


---
常用功能：`button-rj` `button-douban` `button-tu` `button-heian` `button-mingliang`

---
```ad-note
title:我的小白板
icon:fire
collapse:close
<iframe src="https://excalidraw.com" width="100%" height="450" > </iframe>
```


---
# 最近阅读 
```dataview
table without id ("![](" + cover + ")") as Cover, file.link as Name, default(split(author," ")[1],author) as "Author"
from "D3=读书-Reading"  
where status = "在读"
sort file.mtime desc 
```
# 最近收看
```dataview
table without id ("![](" + cover + ")") as Cover, file.link as Name, default(split(director," ")[1],director) as "director" , tags as Tag , progress as Progress
from "D4=观影-Viewing"
where status = "在看" | (status = "已看" & WatchDate>=date(today)-dur(30 days))
sort file.mtime desc
```
---
数据：[[【合集-Buttons】Buttons Set|Buttons合集]] | [[-【MOC-合集】内容MOC合集|MOC合集]] | [[-【Obsidian-资源】Obsidian参考资料合集|OB资料合集]]

---
 