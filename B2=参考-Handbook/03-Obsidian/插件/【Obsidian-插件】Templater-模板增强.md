---
tags: app/obsidian
alias:  Templater
---
**简介：**
Templater 可以执行处理 JavaScript 变量和函数的代码, 并且将结果插入 Obsidian 笔记中

**使用方法：**
[我的Obsidian入门之旅 - 知乎](https://zhuanlan.zhihu.com/p/441013488)
介绍使用之前，这里先把我这里针对模板的配置项信息截图留存一下。
-   一般配置

![](https://pic3.zhimg.com/v2-b0d32c9df4108daa7ad9aaccfbf95106_b.jpg)

  

-   正如一开始介绍目录分配的时候所说，模板存放的位置也应该有一个指定的路径安排，我这里统一将模板文件存放在`zob-config/template`下。
-   `鼠标光标自动跳转`，这个非常重要，非常好用，一定要勾选，后边介绍应用的时候会提到。
-   新建文件应用模板，这个也要勾选，其他日记，周记在快速新建的时候都会用到这个选项。

  
-   模板快捷键

![](https://pic1.zhimg.com/v2-8ef964dd09b24c8c5436422ea1af4898_b.jpg)

  

-   我们可以给指定的模板绑定快捷键，以实现更加快速地应用到模板。

  
-   文件夹模板

![](https://pic4.zhimg.com/v2-6a00288eb098c7836fc7d1a8184a88a3_b.jpg)

  

-   所谓的文件夹模板，其实也可以理解成文件模板，只不过插件更加强大地支持分目录单独配置，我这里针对普通文件目前没有特殊的配置需求，因此就配置了一个模板，作用于整个仓库下的新文件。我们来看下模板内容：

```text
---
author: eryajf
created: <% tp.file.creation_date() %>
aliases: []
tags:
---
 
```

-   启动模板与脚本

![](https://pic2.zhimg.com/v2-44fb6ad15aec6aac52119b336a8b4ae5_b.jpg)

这两个目前还没有具体研究过，所以暂时没有用到。  

-   系统命令功能

![](https://pic3.zhimg.com/v2-baf4a989aaa49cafa07eeb6bec60cc36_b.jpg)

这里非常巧妙地通过配置系统命令，能够为模板系统添加一些更加丰富的能力。比如我这里借助于[wttr.in](https://github.com/chubin/wttr.in)项目的能力，为日历内容中添加了天气信息获取的能力。 由于网站不在国内，获取比较慢，因此我在个人服务器上加了个脚本更新，然后获取天气的方式就变成了从自己的服务器获取，速度快多了。目前提供了如下城市的天气获取，如果你也想借助我这个服务器获取天气，而你的城市又不在列表内，可以评论留言我来添加：  

```text
 北京
 curl -H "Accept-Language: zh-CN" "http://weather.eryajf.net/BeiJing.html"
 上海
 curl -H "Accept-Language: zh-CN" "http://weather.eryajf.net/ShangHai.html"
 广州
 curl -H "Accept-Language: zh-CN" "http://weather.eryajf.net/GuangZhou.html"
 深圳
 curl -H "Accept-Language: zh-CN" "http://weather.eryajf.net/ShenZhen.html"
 杭州
 curl -H "Accept-Language: zh-CN" "http://weather.eryajf.net/HangZhou.html"
 社旗
 curl -H "Accept-Language: zh-CN" "http://weather.eryajf.net/SheQi.html"
```
上边的命令相当于添加了键值对，在模板内容里边，可以通过`<% tp.user.hangzhou() %>`这种方式进行调用。这个模板在日记里边有应用，等到讲解日志插件时候再详细介绍。 另外两个命令是因为我想在周记里边添加上周下周笔记的快捷链接，但是找遍了插件中的说明文档，似乎并没有比较好的方式实现，所以就借助于系统命令的能力，添加了两个数字获取的方法。

**实例：**

**相关：**
* [GitHub - SilentVoid13/Templater: A template plugin for obsidian](https://github.com/SilentVoid13/Templater)
* [[-【Obsidian-插件】Obsidian插件MOC]]