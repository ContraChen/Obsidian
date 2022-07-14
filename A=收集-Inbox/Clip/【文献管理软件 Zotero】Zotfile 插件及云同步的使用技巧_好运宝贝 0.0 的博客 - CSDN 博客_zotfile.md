> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [blog.csdn.net](https://blog.csdn.net/qq_43012930/article/details/114137259)

### 文章目录

*   *   *   [1 前言](#1__1)
        *   [2 下载安装](#2__5)
        *   [3 基本设置](#3__8)
        *   *   [3.1 语言设置](#31___9)
            *   [3.2 常规设置](#32___11)
            *   [3.3 同步设置](#33___14)
            *   [3.4 文件位置](#34__31)
        *   [4 插件](#4__43)
        *   *   [4.1 ZotFile](#41_ZotFile_48)

### 1 前言

本教程是参考了一些博客和官方教程写的，博客链接附在结尾。里面包含了很多概念性的描述，需要带脑子去理解。我觉得 “授人以鱼不如授人以渔”，弄清楚原理才能灵活使用这个软件。**所以本篇不是傻瓜教程！想看傻瓜教程的可以直接叉掉了…**  
PS：因为原本是准备自己看的，没打算上传博客，所以能不插图就不插图了，截图上传挺麻烦的… =_=

### 2 下载安装

在 [Zotero 官方下载链接](https://www.zotero.org/) 里下载并安装 Zotero 独立版以及浏览器对应的 Zotero Connector，同时在官网注册一个账号。

### 3 基本设置

#### 3.1 语言设置

我用的英文版，想改成中文版的在**编辑 - 首选项 - 高级 - 常规**里修改语言即可。

#### 3.2 常规设置

没啥要改动的，勾选上 "Rename linked files".

#### 3.3 同步设置

Zotero 的同步设置分为两种：[同步的官方链接](https://www.zotero.org/support/sync)

*   **Data Syncing：数据同步**  
    数据同步内容可以包含 **文献库的条目、笔记、链接、标签（关键词）** 等等。在 Zotero 中，可以使用 Zotero 提供的同步服务同步除了附件之外的所有内容，以便在不同的支持 Zotero 的设备上使用 Zotero。英文版内容为：[**library items, notes, links, tags**, etc.—everything except attachment files]。此外，还可以登录 Zotero.org 在线查看文献库。**数据同步是免费和无限的，无需文件同步即可使用。** 要注意的操作点有以下几个：  
    (1) 输入自己的 Zotero 账号和密码（在官网注册），点击 “ 开始同步(Set Up Syncing) ” 就开启同步了！  
    (2) “Sync automatically” 的意思是文献库发生变化的时候立刻自动同步，我关掉了，选择自己手动同步，不同时使用两台电脑的话选择自动同步更方便。  
    (3) “Sync full-text content” 网上有人说是同步 PDF 全文内容，但我觉得应该是 **PDF 全文索引的内容**，看官方英文解释：

> When checked, Zotero will sync the contents of the PDF fulltext index, allowing you to search the index across computers and in the zotero.org web library.

*   **File Syncing：文件同步**  
    这个我到后面再详细讲怎么设置，因为还涉及到文件位置、插件设置等内容，这里只介绍概念。数据同步将同步库项目，但不同步附件（PDF，音频和视频文件，图像等）。要同步这些文件，您可以使用 Zotero 文件存储 或 WebDAV 将文件同步设置为伴随数据同步。但官方写了三种同步方式。  
    1.Zotero File Storage：Zotero 官方的网盘，免费 300M。  
    2.WebDAV：国内支持 WebDAV 网盘的只有坚果云，我开始也按照网上的教程注册使用了，直到我发现还有方式 3。  
    3.Linked File Attachments：简单来说，就是用 **ZotFile** 这个插件把链接文件存在 **云同步的文件夹里** ，官方描述如下：

> In your personal library, you can also sync Zotero files across computers using **linked files**. Rather than attaching stored copies of files to Zotero items, **you can attach links to files stored in a cloud-sync folder**, such as Dropbox or Google Drive. When using linked attachments, you should set up Zotero’s **Linked Attachment Base Directory feature** so that Zotero can find your files on each computer, even if the path to **the cloud-sync folder** differs. The **ZotFile** plugin can make managing linked attachments easier by automatically moving attachment files to a designated folder as you import them.  
> **Linked files cannot currently be used in group libraries.**

#### 3.4 文件位置

**编辑 - 首选项–高级–文件和文件夹**

*   先设置**数据存储位置**，默认是在 “C://Users \ 用户名 \ Zotero”，可以设置成自定义的路径，我不想放在 C 盘，就改成了 “D:\xxx\Zotero”。

> *   zotero 的文件分为**普通文件**和**链接文件**（图标左下角会有链接标记）。
> *   所有文件都是存储在该目录下的 storage 文件夹中。
> *   但 zotero 的做法是对每一个条目的所有文件（笔记，附件等）都放在一个**随机命名**的文件夹下，当我们想通过名字找对应的附件的时候就非常不方便了。
> *   zotero 提供了 **zotfile 插件**来解决这个问题，它能**把附件文件变成链接文件，然后进行重命名和归类**。

*   **链接附件的根目录**是存储链接文件的地方，默认是没有设置的。

> *   通过 zotfile 可以将普通附件变成链接附件。
> *   设置成你要放置 zotfile 管理的链接附件（PDF，图片，视频等等）的地方，可以在空间比较大的盘中新建一个文件夹。**如果只用一台电脑的话，其实完全不需要设置这个。**
> *   注意，想要云同步的话，换了电脑后应该设置成**云同步的附件文件夹**。

### 4 插件

所有插件的安装过程都可以归纳成以下两步：：

*   下载插件：下载后缀为 .xpi 的文件；
*   安装插件：打开 Zotero， 工具 -> 插件 -> 点击右上角的齿轮图标 -> Install Add-on From File -> 选中刚下载的 .xpi 文件

#### 4.1 ZotFile

*   **下载地址**：[zotfile 官网](http://zotfile.com/#how-to-install--set-up-zotfile)
*   **功能**：有以下几个功能  
    (1) 自动按照用户设置的格式重命名下载的文件，比如 “作者 - 年份 - 标题”。【这个功能超有用！因为下载的好多论文格式都不对，我以前手动重新命名累死了…】  
    (2) 可以批量重命名文件，以及生成文件的链接。【这个生成链接主要是为了云同步用的】  
    (3) 与 iPad 或 Android 平板电脑同步 PDF。【这个我暂时不用】  
    (4) 在平板电脑上（或计算机上的 PDF 阅读器应用程序）突出显示并注释 pdf 之后，ZotFile 可以自动从 pdf 中提取突出显示的文本和注释注释。【我觉得这个功能也没啥用】
*   **配置步骤**：配置 zotfile，在 “工具 - ZotFile Preferences” 里配置：

**Genreal Settings**：

1.  **Source Folder for Attaching new Files** 是 zotfile 监控文件夹的路径。可以理解成一个临时文件夹，Zotero 会监视这个文件夹，如果有新的 PDF 文献到了这个文件夹里，Zofile 会自动地把它添加到条目里。设置方法网上有两种：  
    (1) 设置为 **zotero 数据存储位置下的 storage 文件夹**，比如 “D:\xxx\Zotero\storage”;  
    (2) 设置成**浏览器的下载目录**，比如 “D:\xxx\google_files”。  
    官方建议是 (2), 那我也按照 (2) 来设置。
    
2.  **Location of Files** 是 zotfile 管理的链接附件文件夹。这个有点难理解，先看看官方说明
    

> ZotFile can _move new and existing attachments to different locations_. You can either **store a copy of your attachment files in Zotero**, which allows you to syns files to zhe Zotero server,or **move the file to a custom folder** and link that location from Zotero".

我的理解是：ZotFile 能把新的或现有的**附件**移动到不同的地方，有两种方式：  
(1) 把附件文件的复制本存在 Zotero 中，从而能用 Zotero 的服务器同步文件；【进行的操作是**对 PDF 进行重命名**但是**不把它从 Zotero 的 Storage 文件夹中移出**，即 PDF 还在原来的 Zotero 文件中，如果使用 WebDAV 同步的话，云盘里会存在 PDF 文件，同时 Zotero 里**不会生成链接**🔗】  
(2) 把文件移动到一个自定义的文件夹，并生成一个链接放到 Zotero 中。【进行的操作是**对 PDF 进行重命名**并且**把它从 Zotero 的 Storage 文件夹中移到指定的文件夹**，即 PDF 已经不在 Zetero 的文件夹里了，而 Zetero 的文件夹里会有 PDF 链接，如果使用 WebDAV 同步的话，云盘里没有 PDF 文件而是只有 PDF 文件的链接，PDF 去了指定的文件夹。子文件夹的命名可以自定义，自定义方式可在 [ZotFile 官网](http://zotfile.com/index.html)进行查询。我设置为`\%c`，这样就可以按目录来保存。】

**现在就来介绍不氪金同步 PDF 的的两种方式！**  
**方式一**：PDF 文件保存在 Zotero 的 Storage 文件夹里 (乱码的子文件夹名称)，用 WebDAV (坚果云) 进行同步，此方法无需下载坚果云客户端，在网页端即可操作。具体过程如下：

**(1) File Syncing 的设置**  
首先，我们需要去坚果云官网注册个人账号。注册好之后在坚果云个人中心的 “账户信息” 中找到 “安全选项” 选项卡。在页面下方的 “第三方应用管理” 中添加一个应用，生成密码。

接下来打开 Zotero 的同步配置，在下方同步方式中选择 “WebDAV”，填入刚才坚果云页面中给出的**服务器地址**和**账户**，密码就是刚才生成的**应用密码**。点击 “Verify Server” 可以验证信息是否填写正确，如果正确会跳出一个窗口提示你云盘上还没有 zotero 这个文件夹，问你要不要新建一个，选择 “create” 即可。

**(2) ZotFile Preferences 的设置**  
选择第一项 “Attach stored copy of files”！

**方式二**：PDF 文件链接保存在 Zotero 的 Storage 文件夹里 (乱码的子文件夹名称)，PDF 文件保存在云同步文件夹里，用第三方云同步软件进行同步 (GoogleDrive，坚果云客户端，OneDrive)，此方法需要下载客户端，所以我选择用 OneDrive，不想下坚果云客户端。具体过程如下：

**(1) File Syncing 的设置**  
这个地方直接不勾选，因为用这个方法存到 WebDAV 上也只是 PDF 链接。

**(2) Files and Folders 和 ZotFile Preferences 的设置**  
“Zotero Preferences - Advanced - Files and Folders” 里的 "**Linked Attachment Base Directory**"和 “ZotFile Preferences - General Settings" 里的 "**Location of Files**" 的文件夹路径都设置为**云同步的文件夹**！比如我的都设置成了 "D:\xxx\OneDrive\folder”.

**tablet settings**：  
这好像是设置平板的，我暂时不用，要用了再补充。

**Renaming Rules**：  
默认是`{%a_}{%y_}{%t}`, 即 “作者 - 年份 - 标题”，但我个人的习惯是把年份放在前面，只要标题，所以改成`{%y_}{%t}`.

*   **使用方法**：

1.  右键文件的 Manage attachment > Rename attachments；
2.  在网页下载的新文件会自动重新命名。
3.  如果要将已链接的文件彻底删除，可以点击 "Tools - Manage Attachments- convert linked files to stored files"，勾选 "delete original file after storing" 后，再全部删除，不然删除的只是链接。  
    ![](https://img-blog.csdnimg.cn/20210227154506421.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzMDEyOTMw,size_16,color_FFFFFF,t_70#pic_center)

参考博客：  
[zotero + 坚果云，免费跨平台文献管理最佳实践指南](https://zhuanlan.zhihu.com/p/112795057)  
[Zotero 配合坚果云 Web DAV 同步那些坑](https://blog.csdn.net/qq_40678163/article/details/108968172)  
[Zotero 5.0 使用教程 / 坚果云同步盘和 Zotero 的配置过程详解](https://zhuanlan.zhihu.com/p/28325366)  
[Zotero 的下载与配置（综合版）](https://blog.csdn.net/qq_44089921/article/details/107954975)  
[我的 Zotero 实践汇总](https://zhuanlan.zhihu.com/p/108366072)  
[Zotero 和 zotfile 插件关联以及使用](https://zhuanlan.zhihu.com/p/104848524)  
[Zotero 文献管理软件总结与安利](https://blog.csdn.net/qq_40678163/article/details/108959891)