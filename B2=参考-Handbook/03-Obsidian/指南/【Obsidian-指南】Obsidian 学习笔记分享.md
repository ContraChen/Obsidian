> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.bilibili.com](https://www.bilibili.com/read/cv15307070/)

> 分享一些有用的内容，成长自己，帮助他人。

> 分享一些有用的内容，成长自己，帮助他人。
> 
>                                                                       ——周树人

最近，我想明白了一个事。把笔记上传到 B 站，不仅了实现跨平台查看笔记，还 TM 是云端存储，这不血赚！！！

————我是🅱️站的大会员的专属分割线🪙🪙🪙————

在 Obsidian 中可设置一至六级标题。`#`号定义重要等级最高的标题，`##`号定义重要等级次高的标题，其他标题依次类推。  
具体写法如下所示：

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

```

要想让常规字体发生倾斜，需要在文本前后各添加一个`*`号。具体写法如下所示：

```
*倾斜字体*

```

在文本前后各添加**两个**`*`号，可使字体变粗。具体写法如下所示：

```
**加粗字体**

```

在文本前后各添加**两个**`=`号，可使字体高亮显示。具体写法如下所示：

```
==高亮字体==

```

用鼠标选中文本后，直接在键盘上按两下`=`号，可将选中的文本变为高亮字体。  
该方法也适用于字体加粗、倾斜等其他样式。

在文本前添加一个`-`号并按一下空格键。具体写法如下所示：

```
- 项目一

```

光标停在无序列表项后时，按回车键会自动生成新的无序列表项。

在文本前添加**整数**并按一下空格键。具体写法如下所示：

```
1. 项目一
2. 项目二
3. 项目三

5. 项目五

```

在有序列表项后回车，会自动生成新的有序列表项。

具体写法如下所示：

```
- [ ] 晨跑20分钟
- [ ] 俯卧撑20个
- [ ] 阅读10分钟

```

打开 Obsidian，其操作界面大致可分为三个区域，如下图所示：

![](http://i0.hdslb.com/bfs/article/53a5c28c30ac742b45c274f7c711f2fd088c0c8a.png@942w_530h_progressive.webp)

左侧栏为文件列表，已创建的文件、文件夹以及导入的图片等都会在文件列表中显示。

右侧栏显示的内容有很多，包括：文本大纲、标签面板、链接面板等。其显示的内容与启用的插件相关。

中间的内容区在官方文档中被称为面板，是我们编辑文本的区域。

Obsidian 支持多面板操作，按住`Ctrl`键并用鼠标点击文件列表的文件名，可打开多个面板。

同一文件也可以打开多个面版进行显示。

用鼠标选中文本后，可使用鼠标进行拖拽。  
在同一面板内拖拽：改变内容显示位置。  
在不同面板间拖拽：复制内容到其他面板。

打开一个文件的两个（或更多）面板时，可设置两个面板相互关联。  
完成关联后，修改其中一个面板另一个面板也会进行相同的修改。

操作方法：点击面板右上角的`更多选项→``与其他面板关联`，再选中要关联的面板即可。（选中可关联的面板时，面板会变颜色。）

取消关联的方法：点击面板右上角的`解除关联`按钮即可。

在 Obsidian 中内置了许多插件，这些插件称为核心插件。Obsidian 中的大多数功能都是靠插件来实现的。

我们可以根据自己需求，可以在`设置→``核心插件`中启用或禁用这些插件。

第三方插件是对核心插件功能上的补充。Obsidian 有着数量庞多的第三方插件，基本上可以满足我们的需求。

要安装第三方插件，首先需要在`设置→``核心插件`中关闭`安全模式`。

**`安全模式`**在 Obsidian 中默认为启用状态。

Obsidian 内部有第三方插件社区， 通过`设置→``第三方插件→``社区插件`可打开插件社区界面。进入社区界面后，便可以自主选择安装所需的插件。

多数情况下，插件社区**因为某些不为人知的原因**并不能够正常使用。此时，若还想使用第三方插件就需要手动下载、安装插件了。

**插件下载**  
通过 OB 插件汇总网站 https://ob.pory.app / 可下载第三方插件。

UP 主 **Johnny 学**也整理了第三方插件下载网页：https://www.airtable.com/embed/shrdmp10Lxmf5Wmgl/tblJqnWpcKURTjysX?viewControls=on

第三方插件内基本上只包含了三个文件，文件名如下图所示：

![](http://i0.hdslb.com/bfs/article/2649ce2c555de61aae4bab62dfbecfebd877d97f.png@782w_197h_progressive.webp)

**安装插件**  
将下载好的插件解压并放置在下图的位置：

![](http://i0.hdslb.com/bfs/article/c740dae8bc9688d60df42691a6ddb8d6d1dd3a84.png@900w_323h_progressive.webp)

值得注意的是，`.obsidian`文件夹为隐藏文件夹，需要设置一下文件夹的显示选项才能看到。如果发现没有`plugins`这个文件夹，就需要自己手动创建一个。

完成以上操作后，重启或刷新软件便可使用插件。

推荐安装的插件：

Note Refactor、QuickAdd、Templater、Advanced Cursors、image auto upload plugin

工作区插件是核心插件之一。启用该插件后，在左侧边栏会多出一个`管理工作区布局`的选项，如下图所示：

![](http://i0.hdslb.com/bfs/article/2004c0b5fbebb8173c3e1b94754be5776111cd99.png@473w_644h_progressive.webp)

该选项允许保存和加载`工作区布局`，该功能类似于 PS 中`工作区`的功能。  
关于工作区的内容在官方文档中有详细说明，所以这里就不做过多的介绍了，只简单说明一下如何开启工作区这个功能。  

点击左侧边栏的**`帮助`**按钮可查看官方文档。

开启方法：在左边边栏的`设置→``核心插件`中找到并启用工作区插件即可，如下图所示：

![](http://i0.hdslb.com/bfs/article/42dea65aff614af311c1898a41f914ce492ca345.png@942w_95h_progressive.webp)

链接是 Obsidian 中的核心功能之一。该功能在官方文档中有着大篇幅的描述和讲解，详细说明可以去查看官方文档。

链接 Obsidian 中的其他文件的方法有两种。  
方法一，在文件中输入要链接文件的文件名，在该文件名前后添加**两个**`[`号。具体写法如下所示：

```
[[文件名]]

```

方法二，用鼠标选中任意文本，再使用键盘直接输入**两个**`[`号（英文输入法），被选中的文本就会被变成链接。此时，该文本只是在样式上发生了变化，实际上并没有链接到任何文件或内容上。

之后，按住`Ctrl`键并用鼠标点击该文本（编辑视图模式下），在文件列表中会以选中的文本内容为文件名，自动新建一个文件并显示该文件的面板。

当面板在编辑视图的模式下，按住**`Ctrl`**键并用鼠标指向连接，可以预览文件内容；鼠标点击后会跳转到所链接的文件。  
当面板在阅读视图的模式下，仅使用鼠标即可实现预览和跳转功能。

通过第三方插件 Note Refactor，可根据文本中的一、二和三级标题快速创建文件并将标题链接到所创建的文件上。

安装好插件后，在`设置→``Note Refactor`中根据个人需求设置新建文件的存储位置，如下图所示：

![](http://i0.hdslb.com/bfs/article/36446121b3713a471c1fd84b83c24f20fbccac53.png@942w_795h_progressive.webp)

完成设置后，即可使用该功能。通过在命令面板中输入`note`可查看 Note Refactor 插件的相关命令，如下图所示：

![](http://i0.hdslb.com/bfs/article/0cf066261bf11da227cf2f6427933797ae78e622.png@942w_593h_progressive.webp)

选中上图红框中的命令即可根据文本中的标题来创建文件。点击标题便可跳转到所链接的文件的面板。

通过使用插件 Note Refactor 的功能，再配合使用思维导图，便可根据大纲快速生成所需文件。

先用思维导图这类工具软件写好题材的大纲，再将大纲导出成 markdown 格式的文件，将其内容导入或复制到 Obsidian 中，大纲会自动变成标题。

通过插件 Note Refactor 便可根据大纲内容创建文件。

使用 XMind 软件可以导出 md 文件。

选中文本，右键选择`将当前选中内容移动到其他文件中`，可以根据所选文本内容创建新文件并在原文本位置生成链接到新文件的链接。

在`[[]]`符号中输入`^^`这两个上三角符号。可以检索所有的文本块，在其后输入内容，可以搜索到输入内容的文本块。

![](http://i0.hdslb.com/bfs/article/545a2eac2bef7b4542e883d80b758e451f668d98.png@926w_626h_progressive.webp)

当链接的名称不符合自己要求时，我们可以通过为链接设置别名对链接名称进行修改。

先在链接名称后添加`|`符号，再在`|`符号后添加自己想要其显示的名称，也就是别名。具体写法如下所示：

```
[[文件名|新的文件名]]

```

完成修改后，链接在阅读视图模式中的显示的名称就是`|`符号后面输入的内容。

可以在被链接文件的 yaml 区添加多个别名，在修改其链接名称时，可在添加的多个别名中进行选择，增加了设置别名的灵活性。

yaml 区一搬创建在文本的开头，具体写法如下所示：

```
---
填写信息区域
---

```

首先在被链接文件的 yaml 区添加一个或多个别名，写法如下所示：

```
---
aliases: 别名一,别名二
---

```

在 yaml 区添加好别名后，文件在阅读视图模式中的显示效果如下图所示：

![](http://i0.hdslb.com/bfs/article/ece2923c60f1c42229f711793f172097491d159a.png@942w_270h_progressive.webp)

之后，在修改该文件的链接名称时，输入`|`符号后便可在添加别名中进行选择，如下图所示：

![](http://i0.hdslb.com/bfs/article/d7033359ced67dfca64791567d1534467d778bc8.png@722w_320h_progressive.webp)

关于 yaml 我自己并没有了解太多，仅知道在 Obsidian 中的部分用法，这里就不做过多介绍了。

将被链接文件中的内容显示到当前文件中，这种显示方法称为嵌入。

在文件链接的前面添加感叹号（英文输入法），可具体写法如下所示：

```
![[文件名]]

```

在编辑视图模式下显示的效果如下：

![](http://i0.hdslb.com/bfs/article/e79384cbccfa53aa5f85df606bb7068b1b20c595.png@942w_509h_progressive.webp)

图片通过复制或直接拖拽便可嵌入到文件中。  
嵌入文件中的图片，在默认情况下是存储在当前库的根目录下。其存储位置可以在在`设置→``文件与链接`中进行修改。

![](http://i0.hdslb.com/bfs/article/a2e41550e6c48932339c37e705e2f035771392d1.png@942w_470h_progressive.webp)

Obsidian 支持修改嵌入图片显示效果的大小。当图片的大小不符合要求时，可以进行修改。

在图面名称后添加`|`符号，之后在`|`符号后设置图片的宽度。具体写法如下图所示：

![](http://i0.hdslb.com/bfs/article/e46ee5ea33b659fc2373467790ff029e835e5a38.png@768w_374h_progressive.webp)

上图中的`|`符号后面的`600`表示宽度，高度会等比例变化。也可以同时修改宽和高，在图片名后面输入`|500x300`，其含义为将图片的宽设置为 500，高设置为 300。

图床作为辅助 Obsidian 使用的工具，需要单独下载安装。其作用是将文件中的图片上传到云端保存并自动把图片转换成链接。

文件中用到的图片上传到图床后，可从图床上复制图片的链接并将其复制到文件中，完成后即可显示图片。如此一来，即使在其他电脑上没有存储文件中的图片，也能查看完整的文件内容。

这里介绍一种图床工具 PicGo，PicGo 下载网址：https://molunerfinn.com/PicGo/。

**自动上传**

图床可以单独使用，也可以配合 Obsidian 的第三方插件 image auto upload plugin 一起使用。

安装好 image 插件后，在`设置→``第三方插件`中启用插件并打开其设置界面，如下图所示：

![](http://i0.hdslb.com/bfs/article/190c7ce63f37a64b31b071054d8e552e1e27f5e1.png@942w_200h_progressive.webp)

完成设置后，只要将图片复制到 Obsidian 中，该图片就会自动上传到图床。在文件中会自动嵌入该图片的链接，省去了手动操作的步骤。

**设置哔哩哔哩图床**  
哔哩哔哩图床是免费的，但哔哩哔哩图床是第三方图床，需要手动修改 PicGo 的配置。

第一步，先在 PicGo 的`插件设置`中下载哔哩哔哩插件。

第二步，在`bilibili图床`中查看配置教程，如下图所示：

![](http://i0.hdslb.com/bfs/article/7139f1f39c1f233302bf7676a55c66c6bca9a068.png@942w_530h_progressive.webp)

第三步，在`PicGo设置`中选择使用 B 站图床。

![](http://i0.hdslb.com/bfs/article/f703fbff5d3eaa840497ea6a894df4732cdc8f58.png@942w_531h_progressive.webp)

使用第三方插件 Banners，可实现在文件顶部位置中插入图片的功能。效果如下图所示：

![](http://i0.hdslb.com/bfs/article/a57c35c3fa8b4bf0a700c8605a459a58abf10ff5.png@942w_402h_progressive.webp)

第一步，先安装插件 Banners，完成安装后在`设置→``第三方插件`中启用插件。

![](http://i0.hdslb.com/bfs/article/bec398f6d09319852a443a42c645b2de2cd88c74.png@942w_129h_progressive.webp)

第二步，打开命名面板，使用插件 Banners 的命令将图片导入到文件中。

![](http://i0.hdslb.com/bfs/article/105f4ff7ae9385ea9c4783954d15b17c3334081b.png@878w_218h_progressive.webp)

完成上述操作，图片就能作为头图显示了。在 Banners 插件的设置页可以对头图的高度和样式进行设置，如下图所示：

![](http://i0.hdslb.com/bfs/article/df58243cb43317ff384c2d116eea33a50f50218a.png@942w_330h_progressive.webp)

轮播图的显示效果如下图所示：

![](http://i0.hdslb.com/bfs/article/3c2ef307fa7c5e53d2d4a2a4bf588f18f2d36156.png@914w_477h_progressive.webp)

若要在文件中嵌入轮播图，需要用到网站：https://www.canva.cn/。

第一步，在 Canva 网站新建画布，设计好轮播图。如下图所示：

![](http://i0.hdslb.com/bfs/article/17f81ecd02643e73b2be1cf31778371a1cca398f.png@651w_405h_progressive.webp)

第二步，将复制轮播图的嵌入代码。

![](http://i0.hdslb.com/bfs/article/5f72890a9200aad28cd927d7ca5a676f6eb83d21.png@552w_770h_progressive.webp) ![](http://i0.hdslb.com/bfs/article/b69ff7887479b2456dd2a8f44007e0eda24d1f98.png@534w_428h_progressive.webp)

将代码粘贴到文件中便可显示轮播图。

Obsidian 支持对视频的嵌入与播放。  
第一步，先获取视频的嵌入代码。嵌入代码一般在页面的分享功能中，如下图所示：

![](http://i0.hdslb.com/bfs/article/380db418fd5f04c86618e20b7177464e224ecffc.png@789w_443h_progressive.webp)

嵌入代码的样子，大致如下代码所示：

```
<iframe src="https://player.bilibili.com/player.html?aid=720241593&;amp;bvid=BV1KQ4y1a7pd&cid=401115360&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

```

第二步，将嵌入代码粘贴到文件中。

在导入 B 站视频的代码时，需要手动添加一些信息，如下图所示：

![](http://i0.hdslb.com/bfs/article/1142bb0f889df23869053b5d1694e8157d8e5473.png@849w_203h_progressive.webp)

将代码粘贴到文件中后，便可播放视频。

若对文件中视频的大小不满意，还可以修改其宽高。修改方式如下图所示：

![](http://i0.hdslb.com/bfs/article/ba3a95ddb88929a62718b5df36a1beefec44facc.png@875w_159h_progressive.webp)

`width`表示视频的宽度，`height`表示视频的高度。

标签的主要作用是：让我们更容易找到笔记。关于标签功能在官方文档中也有详细的说明。

要使用标签，首先需要在`设置→``核心插件`中找到并启用标签插件。启用后，在右侧栏中就会显示出标签面板。

给文件添加标签的方法有两种。  
方法一，在文件的任意位置（一般会在文件的开头或结尾），输入`#`号（不空格）并输入标签名。可具体写法如下所示：

```
#标签名

```

方法二，在 yaml 区添加标签。  
在 yaml 区添加标签的具体写法如下所示：

```
---
tags: 标签一 "#标签二"
---

```

在 yaml 区，如果要给标签加上`#`，就要使用双引号，不然会被当作是注解。

在 yaml 区添加标签的好处是：当导出的文件时，yaml 区中的内容不会显示在文件里。该方法可以让文件导出后，不显示标签名。

通过在标签中插入`/`符号，给标签设置层级。具体写法如下所示：

```
#状态/计划中 #科目/英语 #科目/数学

```

设置标签层级后，可在标签面板中查看层级显示效果，如下图所示：

![](http://i0.hdslb.com/bfs/article/6462de9f6575a5fefc920f489764638af675e3cf.png@368w_351h_progressive.webp)

设置标签层级，有助于我们通过标签面板更加快捷地查询内容。

要使用模板，首先需要在`设置→``核心插件`中找到并启用模板插件。  
启用后，点击启动按钮旁边的`⚙`按钮，进入设置界面。  
在`模板文件夹位置`中，为存放模板文件的文件夹取名。完成后，在文件列表中会自动创建该文件夹。

完成上述设置后，在新建的文件夹中创建文件并编写内容，该文件便是一个可用的” 模板 “。

在新建文件后，使用`Ctrl+P`打开命令搜索框，在搜索框中输入`模板`便可查询到`插入模板`命令，如下图所示：

![](http://i0.hdslb.com/bfs/article/93567961496c39417b29b4d73f10ccc76cf30722.png@942w_297h_progressive.webp)

使用`插入模板`命令，即可将作为模板的文件中的内容复制到新建文件中。

在编写模板文件的内容时可使用占位符。在 Obsidian 中可使用时间、日期等多种占位符。

占位符可理解为在文本中先占据一个固定的位置，等待往里添加内容的符号。

有时，在模板文件中需要使用日期、时间等每天发生变化的信息。占位符的使用可以来代替这些变化的信息编写在模板文件中。  
当使用模板文件时，占位符会自动变成当天的集体日期、时间等信息。

模板文件中的占位符写法如下所示：

```
# {{title}}

{{date}}

{{date:YYYY-MM-DD}}

{{time}}

```

上述案例中，`# {{title}}`的作用是表示一级标题。  
`{{date}}`的作用是表示当前日期。  
`{{time}}`的作用是表示当前时间。  
`{{date:YYYY-MM-DD}}`的作用是表示当前日期并已`YYYY-MM-DD`的格式显示。

占位符除了可以直接编写在文件中，还可以编写在 yaml 区里。具体写法如下所示：

```
---
data: {{date}}

time: {{time}}
---

```

使用第三方插件 Templater，可实现自动插入指定模板内容到新建文件的功能。

安装好该插件，在`设置→``第三方插件`中启用插件并打开其设置界面，如下图所示：

![](http://i0.hdslb.com/bfs/article/774337661c03008670f61cce362851bdbd014bfb.png@942w_356h_progressive.webp)

在设置界面中，第一步需要先添加模板文件夹的位置。

![](http://i0.hdslb.com/bfs/article/74827d37ae250d61cd0ebfc04521372f81d21b0f.png@942w_122h_progressive.webp)

这里的模板文件夹就是**`核心插件→``模板`**中所设置的模板文件夹。

第二步，启用`Trigger Templater on new file creation`功能。

![](http://i0.hdslb.com/bfs/article/42068a6ba4ebb6b2a7aeacc409bedbb678e67773.png@942w_107h_progressive.webp)

该功能启用后，在界面下方会弹出新的设置项，如下图所示：

![](http://i0.hdslb.com/bfs/article/1fce5504825a2c76baf60fc8c84ebdddf6e1bd24.png@942w_243h_progressive.webp)

第三步，点击右下角的加号。在新出现的第一个文本框中填入文件名称，如：W。在第二个文本框中填入模板名称，如：M。操作如下图所示：

![](http://i0.hdslb.com/bfs/article/559b4b1869f602562ac51dda2afd2ea7aa8ff9fe.png@942w_135h_progressive.webp)

此操作是将文件夹与模板进行关联。通过点击加号，可以保存多组文件夹与模板的关联设置。

完成设置后，当我们在 W 文件夹中新建文件时，文件中会自动插入 M 模板的内容。

使用第三方插件 QuickAdd，可实现插入部分文本内容到文件的功能。

先安装好该插件，在`设置→``第三方插件`中启用插件 QuickAdd 并打开其设置界面，如下图所示：

![](http://i0.hdslb.com/bfs/article/e87bf1cf3347f8b805deb0fb5a5d83dbda9de3d4.png@942w_254h_progressive.webp)

在设置界面中，第一步先按下图所示流程操作：

![](http://i0.hdslb.com/bfs/article/bb743d46e3278fa57ac1f9c28da0286740998149.png@942w_228h_progressive.webp)

第二步，打开设置界面，如下图所示：

![](http://i0.hdslb.com/bfs/article/9d7b150397a357790e77800ebc01c63386c129c5.png@444w_194h_progressive.webp)

第三步，启用相关功能：

![](http://i0.hdslb.com/bfs/article/26643cf9e4460db4a5d6fe8c8d82f7cabc96dac2.png@942w_333h_progressive.webp) ![](http://i0.hdslb.com/bfs/article/684083d86022e129054adebdcf3fd60ae953cefd.png@942w_374h_progressive.webp)

可输入的模板内容，案例如下：

```
姓名：{{VALUE}}
年龄：{{VALUE}}

```

其中`{{VALUE}}`为占位符，表示需要输入的内容。

输入的模板内容时想要换行，需要按 shift + 回车键。

添加好模板内容后，回到上一界面，点击⚡闪电图标，如下图所示：

![](http://i0.hdslb.com/bfs/article/0c6fddc56fac5e1b9a9cf4308deee98baf6b3e15.png@942w_140h_progressive.webp)

完成这一系列设置后，打开命令模板，使用 QuickAdd 插件的命令。

![](http://i0.hdslb.com/bfs/article/8e0e6ba7808e788a8d7e197fa52cc5bbe46f986a.png@942w_500h_progressive.webp)

使用命令后，会弹出输入框，如下图所示：

![](http://i0.hdslb.com/bfs/article/6e6fdd6228f5b37893eced15f87924124a1754dd.png@942w_425h_progressive.webp)

在输入框中输入的内容便是占位符 {{VALUE}} 的值。

输入完内容后，便完成了模板的插入。通过这个方法，可以在文件中的任意位置插入所设计的模板内容。

对于模板内容，还可以为每个要输入的数据设置别名，案例如下：

```
姓名：{{VALUE:姓名}}
年龄：{{VALUE:年龄}}

```

其中`:姓名`中的`姓名`为设置的别名。

设置好别名后，在弹出的输入框中会显示：

![](http://i0.hdslb.com/bfs/article/e1e757acf3774f0e89fdab858140a3f7c0aa16ff.png@942w_273h_progressive.webp)

在文件中可以插入搜索内容并可进行跳转查看内容。具体写法如下图所示：

![](http://i0.hdslb.com/bfs/article/19ef5c4c353bac1c3ab880e77d07d74c2c9d2b27.png@228w_111h_progressive.webp)

添加该内容后，在阅读视图模式中会显示搜索结果，如下图所示：

![](http://i0.hdslb.com/bfs/article/d4a33f00fe7876f87b538e7c727a6a779d31d95e.png@767w_278h_progressive.webp)

在搜索内容中还可以添加查询条件，如下图所示：

![](http://i0.hdslb.com/bfs/article/305bb55cca9a979f20cef929d60f3dfde45e9c4f.png@177w_111h_progressive.webp)

上图中，`path:模板`含义是在`模板`文件夹中查询。

在阅读视图模式中会显示效果如下图所示：

![](http://i0.hdslb.com/bfs/article/6e918f5f23c7116e72c87be37c725f0c6a538507.png@942w_218h_progressive.webp)

点击面板右上角的`更多选项→``打开局部关系图`可查看当前文件与链接文件之间的关系图谱。

关系图面板左上角的`筛选→``深度`，调节该参数大小可控制显示的链接层级。该参数位置如下图所示：

![](http://i0.hdslb.com/bfs/article/5f2cea6e01d10027f801f5358acefbe2d95321fc.png@384w_432h_progressive.webp)

在关系图中，默认只显示与本文件相关的链接。

粘贴纯文本：Ctrl+Shift+V

打开命令搜索框：Ctrl+P

调整字体大小：Ctrl（按住）+ 鼠标滚轮

返回到上一文件：Ctrl+Alt + 左方向键

跳转到下一文件：Ctrl+Alt + 右方向键

多行同时编辑：Alt 键（按住）+ 鼠标点击

重命名笔记文件：F2

重新加载命令，如下图所示：

![](http://i0.hdslb.com/bfs/article/c7c7aa651467cb3ddf5c7d5857f43e817bb6020e.png@905w_288h_progressive.webp)

Templater 插件还可实现控制光标移动的功能。

第一步，打开插件设置界面，启用`Automatic jump to cursor`功能。

第二步，新建模板文件，在文件中输入`<% tp.file.cursor(...) %>`。案例如下：

```
姓名：<% tp.file.cursor(1) %>
性别：<% tp.file.cursor(2) %>
年龄：<% tp.file.cursor(3) %>

```

第三步，在`设置→``快捷键`中，查询该功能的快捷键。

![](http://i0.hdslb.com/bfs/article/59b64a8f9a64aafe1fffd844a399148583a0f5bf.png@942w_158h_progressive.webp)

完成设置后，在文件中导入上述模板内容。使用快捷键，光标会自动移动到`<% tp.file.cursor(1) %>`的位置。第二次使用快捷键，光标移动到`<% tp.file.cursor(2) %>`的位置，以此类推。

![](http://i0.hdslb.com/bfs/article/4ef112e2f1a51f8d1a6b157b842d446dd3856d84.png@575w_342h_progressive.webp)

使用第三方插件 Advanced Cursors，可实现快速选中任意数量的内容相同的文本的功能。

安装好该插件后，在`设置→``快捷键`中设置好该功能的快捷键，如下图所示：

![](http://i0.hdslb.com/bfs/article/b3f202c6939a31868f6886685c4e92926b579442.png@942w_146h_progressive.webp)

完成设置后，先用鼠标选中内容。之后，每按一次快捷键便会多选一个相同的内容。

![](http://i0.hdslb.com/bfs/article/c1407b3f52d023e63ad0c631d9b186e51adabb63.png@779w_755h_progressive.webp)

选中后，可同时修改其内容。

Note Refactor 插件还可实现批量创建链接文件的功能。

第一步，打开插件设置界面，设置新建文件的存储位置。

![](http://i0.hdslb.com/bfs/article/69d47e26ddbe700d92f3538a9672fe1adb4acc7e.png@942w_74h_progressive.webp) ![](http://i0.hdslb.com/bfs/article/c002b20fa538769f1ef861c1739bb681f985ecc9.png@942w_198h_progressive.webp)

存储位置有三种设置方式，上图说明了两种，还有一种是将生成的链接文件放置在根目录下。这一步设置需根据自身需求来选择设置方式。

第二步，打开命令模板，调用 Note Refachor 命令来批量生成链接文件。

![](http://i0.hdslb.com/bfs/article/6b31ded5adfc8b10b0248d76c3d8b0056ece21dd.png@942w_462h_progressive.webp)

生成链接文件将保存之前设置的存储位置中。

————我是🅱️站的大会员的专属分割线🪙🪙🪙————

本篇笔记的内容源于 b 站 UP 主 [Johnny 学](https://space.bilibili.com/432408734)的教学视频，番号：[BV1i3411k7TQ](https://www.bilibili.com/video/BV1i3411k7TQ?from=articleDetail)。该 UP 主讲解很不错，初次学习 Obsidian 的小伙伴可以通过番号去搜索视频学习。

我记笔记的主要目的是为了方便自己日后回顾知识点，本篇笔记中记录的都是我个人认为比较重要的知识点。因此，这篇笔记所记录的内容并不完善，可能对于刚接触 Obsidian 的小伙伴并不友好。但作为回顾 Obsidian 使用技巧的复习资料，本篇笔记还是值得收藏的，希望能够帮助到学习使用 Obsidian 的各位。

在学习使用 Obsidian 的过程中，给我最直接的感受就是软件功能强大了，学习成本也变高了。如果有小伙伴知道哪些功能强又简单好用的笔记软件，望能在评论区分享一下。

GIF

![](http://i0.hdslb.com/bfs/article/49740d99cc07539a66e4cd2b1c0c93df94a35d8f.gif)

————我是🅱️站的大会员的专属分割线🪙🪙🪙————

最后的最后，我还有个秘密要说。那就是在今年过春节的时候.......

别人去拜年的时候，我在家学 Obsidian！

别人吃大餐的时候，我在家学 Obsidian！

别人收红包的时候，我还在家学 Obsidian！

真人真事！！！真人真事！！！真人真事！！！

这就是我回家过年期间所发生的故事，这是我与 Obsidian 之间可以说的秘密。

都这么说了，让我参加个专栏春节征稿活动不过分吧。