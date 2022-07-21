---
tags: app/obsidian,pending 
alias:  Buttons
---
**简介：**
能够提供一个多功能的按钮，你可以给按钮绑定任意的操作。

**使用方法：**
通常这个插件应该会是出现在固定的首页里边，我们能够简单高效地通过点击按钮执行一些操作。

正如开始截图的个人主页那样，借助于QuickAdd插件的捕获功能，我将按钮绑定在对应功能的快捷键上，从而提供了类似闪念胶囊的作用。

打开命令面板，输入`按钮`(如果没有汉化则输入button)，可以进入如下选项页：

  

![](https://pic4.zhimg.com/v2-2d062a7696f1eed8c006ccd965898cab_b.jpg)

  

添加成功之后，会生成如下代码块：

````text
```button
name 闪念
type command
action 快速添加: 日常随思
color blue
```
^button-m6g9
````

我这里是在汉化仓库下载的插件，中文用起来还是更加丝滑一些。

通常之后再添加同样的常规按钮，则直接复制如上配置块儿信息，改下`name`，`action`，以及最后的`^button-m6g9`即可，最后的这个是这个button的唯一ID，我们可以通过`button-m6g9`这个ID全局调用这个button。

这样把按钮放到首页，点击按钮即可直接创建一条短记到指定笔记中。

同理，套用这个命令功能，事实上所有我们在命令面板执行的命令，都可以通过这种方式绑定到按钮上。

**实例：**
[[【合集-Buttons】Buttons Set|Buttons Set]]
![](https://obsidian-001-1312884387.cos.ap-nanjing.myqcloud.com/ImageBed/20220720173738.png)


**相关：**
* [[-【Obsidian-插件】Obsidian插件MOC]]