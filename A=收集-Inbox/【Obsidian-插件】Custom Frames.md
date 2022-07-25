---
tags: app/obsidian,pending 
alias:  Custom Frames
---
**简介：**


**使用方法：**


**实例：**


**相关：**
* 所用插件 custom frames obsidian://show-plugin?id=obsidian-custom-frames
* https://github.com/Ellpeck/ObsidianCustomFrames 
* [[-【Obsidian-插件】Obsidian插件MOC]]

**代码：**
修改滚动条的css
```css
* {  scrollbar-width: thin;  scrollbar-color: #48aefc #DFE9EB; } /* Chrome, Edge and Safari */ *::-webkit-scrollbar {  width: 10px;  width: 10px; } *::-webkit-scrollbar-track {  border-radius: 5px;  background-color: #DFE9EB; } *::-webkit-scrollbar-track:hover {  background-color: #B8C0C2; } *::-webkit-scrollbar-track:active {  background-color: #B8C0C2; } *::-webkit-scrollbar-thumb {  border-radius: 5px;  background-color: #48aefc; } *::-webkit-scrollbar-thumb:hover {  background-color: #48aefc; } *::-webkit-scrollbar-thumb:active {  background-color: #48aefc; }
```
屏蔽flaticon广告
```css
.edge-content-icon-list{visibility:hidden !important; position: absolute !important;}
```