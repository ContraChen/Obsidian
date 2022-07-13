> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/347493385) ✍️  回答于 4 天前
>相关资源 [wwa.lanzoui.com/b016ojl](http://link.zhihu.com/?target=https%3A//wwa.lanzoui.com/b016ojlkh)  密码:dfc3

**2021.3.13** 翻译器更新需要勾选【Enable Logging】和【Show in Console】再进行更新。

![](https://pic4.zhimg.com/v2-540ce2267cf2e5648b9df9c78683221f_r.jpg)

随着深入使用 Zotero，我认为 Zotero 已经成为了我个人知识管理系统的**中枢**。

除了基础的文献管理功能，借助 Zotero 我还可以联结自己的笔记系统、阅读体系。在分开生活与科研需求后，Zotero 甚至还成为我专属的科研收藏夹、科研 RSS 阅读器……

> 工欲善其事，必先利其器。

我一向认为科研软件非常重要，作为中文系的学生也**同样**需要学习最前沿的尖端软件帮助完善自己的工作流、提高自己的科研效率，“**数字人文**”（Digital Humanities）专业以及方法的兴起同样佐证了我的观点。

这里的 “提高效率” 并非是“伪效率”，阅读并按照本文完成 Zotero 学习所需的时间**远小于** Zotero 可以帮你节约的时间。仅以插入参考文献为例，【Zotero 抓取条目—进入文字处理软件插入参考文献—导出参考文献】这一流程的效率远高于【手动输入】或是【知网导出】。而且 Zotero 附带的文献管理功能以及存储功能保留了你的科研足迹，使得你的数据可以重复使用。

Zotero 本身是一款诞生于英文环境的文献管理软件，但高自由度和良好的生态环境让 Zotero 社区开发了许多实用的插件使得处理中文环境同样得心应手。Zotero 学习的难点就在于**配置**好使用环境。

本文分为三个部分，旨在帮助并未接触过文献管理软件的科研小白快速**配置**好 Zotero 并粗略掌握**使用技巧。**如果已经使用过 Zotero 并想要深入学习使用技巧，推荐阅读：

[RefTools](https://zhuanlan.zhihu.com/reftools)[青柠学术 - Zotero | 打造最佳文献生态](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/mp/appmsgalbum%3F__biz%3DMzAxNzgyMDg0MQ%3D%3D%26action%3Dgetalbum%26album_id%3D1319074508795641857%26scene%3D173%26from_msgid%3D2650457410%26from_itemidx%3D1%26count%3D3%23wechat_redirect)![](https://pic2.zhimg.com/v2-4bf4f2680598bfb3a97ff5afd14ebed1_r.jpg)

本文涉及的安装包

[密码: wcj4](https://link.zhihu.com/?target=https%3A//pan.baidu.com/s/1qbf6dj-rvaezSb84UCX7Pg)

1 为什么选择 Zotero？
---------------

### **1.1 常见的文献管理软件有哪些？**

*   [研究生必备文献整理工具 - 卷卷的文章 - 知乎](https://zhuanlan.zhihu.com/p/105066833)
*   [常用的几款文献管理软件 Citavi 、Mendely、Endnote、Refworks、Zotero、Papers 功能大比拼！哪个最好用？](https://link.zhihu.com/?target=https%3A//www.softhead-citavi.com/blog/2314)

### **1.2 为什么我只推荐 Zotero？**

### **1.2.1 你的需求是什么？**

*   语言环境

*   中文环境？——NoteExpress？知网研学？
*   英文环境？——Endnote？Zotero？Mendely？

*   开源 / 商业软件

*   开源？——Zotero？
*   商业？——NoteExpress？Endnote？

### **1.2.2 NoteExpress**

*   基本功能：[求推荐一款文献管理软件? - Puppy 的回答 - 知乎](https://www.zhihu.com/question/370149844/answer/1447727007)  
    
*   优点：中文数据库的直接检索  
    

*   题录→文献（Zotero 可以通过更多步骤实现）

*   缺点  
    

*   非开源软件
*   垃圾的优化、网速、配置
*   难看的界面

*   只支持 PC 端

### **1.2.3 知网研学**

*   强制捆绑知网软件

*   硕博论文只能下载 CAJ 格式
*   批量下载捆绑知网研学

*   垃圾的优化
*   非开源软件

**选择 Zotero 的两大理由**：

1.  开源：自由度高，生态环境好，社区已经有很多实用插件，可以实现可能性高
2.  免费：免费才是硬道理

2 下载安装及环境配置
-----------

### **2.1 下载安装**

### **2.1.1 本体：**[Zotero](https://link.zhihu.com/?target=https%3A//www.zotero.org/) **下载**

Zotero 官网速度较慢，建议使用**网盘**中【Zotero-5.0.95 版】Windows 和 Mac 系统的安装包进行安装。

### **2.1.2 浏览器插件：**[Zotero Connector](https://link.zhihu.com/?target=https%3A//www.zotero.org/download/connectors) **下载**

*   Chrome：需翻墙，crx 文件见**网盘**。
*   Edge：无需翻墙。
*   Firefox：无需翻墙。

### **2.1.3 翻译器：**[Zotero translators_CN](https://link.zhihu.com/?target=https%3A//github.com/l0o0/translators_CN) **下载**

可略过此步，现中文翻译器可以通过【**茉莉花**】插件实现。

**翻译器更新**（以 Chrome 为例）：

在翻译器更新后（即【手动】覆盖或【茉莉花】插件覆盖后）需要进行【Update Translators】。

1.  单击右上角【Zotero Connector】插件（建议固定【Zotero Conncetor】）
2.  单击【选项】
3.  进入【Advanced】
4.  找到【Translators】，点击【Update Translators】
5.  退出浏览器，重新进入，翻译器更新完成

![](https://pic3.zhimg.com/v2-132c2408e63b21c409d65fea3ab0954e_r.jpg)

### **2.1.4 文字处理软件插件：Microsoft Word 插件下载**

1.  打开【Zotero】
2.  进入【首选项】（Mac 快捷键`command+,`）
3.  进入【引用】—【文字处理软件】
4.  安装加载项【Microsoft Word】或【LibreOffice】

![](https://pic1.zhimg.com/v2-6eb6a4c96a35de2c39a8168d7df90b64_r.jpg)![](https://pic3.zhimg.com/v2-20cf6ad34f6643b8acc0702058b49936_r.jpg)

### **2.1.5 Zotero 插件：Zotero 插件推荐及下载**

插件包见**网盘**。

插件安装：

*   方法一：

1.  打开【Zotero】
2.  点击【工具】—【插件】
3.  点击右上角【⚙】—【Install Add-on From File…】—选中需要安装的插件（部分插件不适用该方法）
4.  安装完毕后重启【Zotero】

![](https://pic4.zhimg.com/v2-d939b36322b73e0262dd53810bb431d7_r.jpg)![](https://pic2.zhimg.com/v2-4f6e9ee485a0f9b2cfa6ed7e68c859e5_r.jpg)

*   方法二：

1.  打开【Zotero】
2.  点击【工具】—【插件】
3.  将需要安装的插件【拖动】至该页面
4.  安装完毕后重启【Zotero】

**2.2 环境配置**

### **2.2.1 本体：Zotero 环境配置**

打开【Zotero】—进入【首选项】（Mac 快捷键`command+,`）

【常规】：建议保持不变

![](https://pic2.zhimg.com/v2-d296bbbd4314d0ed7e705f99dedf1e61_r.jpg)

【同步】

1.  【数据同步】：创建并登陆你的【Zotero 账户】 建议开启【自动同步】和【同步全文内容】
2.  文件同步 Zotero 只提供 300MB 的免费存储空间，建议使用【WebDAV】同步文献库中的附件。

![](https://pic2.zhimg.com/v2-d644c7569506590789f9c98f219139e5_r.jpg)

这里推荐使用【[坚果云](https://link.zhihu.com/?target=https%3A//www.jianguoyun.com/)】，坚果云免费版提供 1GB / 月的上传流量和 3GB / 月的下载流量。

1.  注册【坚果云账户】
2.  点击右上角【用户名】—进入【账户信息】

![](https://pic3.zhimg.com/v2-a7d5bbb11d3e5f3cfdca116f76ba2bd2_r.jpg)

3. 进入【安全选项】

4. 向下拖动进入【第三方应用管理】—点击【添加应用】—输入应用名【Zotero】 这里【示例】中的【服务器地址】、【账户】和【密码】（应用密码）即是【WebDAV】需填写的【URl】、【用户名】和【密码】

![](https://pic2.zhimg.com/v2-b018f278187aca40311122b632f74309_r.jpg)

5. 返回【Zotero】—【首选项】—【同步】 将【同步文献库的附件】改为【WebDAV】，输入【URl】、【用户名】和【密码】，点击【验证服务器】成功即可。

若遇到验证失败，可参考

*   [青柠学术 - Zotero | 用坚果云无限扩展文献存储空间](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/SPKEtNTtFZgd7zIXbxSJfg)
*   [青柠学术 - 方法更新｜Zotero 或者 PaperShip 绑定坚果云 WebDAV 时，验证失败怎么解决？](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/2QhDmtWu6ISgDZ9FrIdIBw)

【引用】

*   点击【获取更多样式】可以下载 Zotero 官方引用样式

1.  点击【获取更多样式】
2.  搜索【7714】即可安装国标引用样式。 注意有 1987、2005 和 2015 三个时间，note、author-date 和 numeric 三个格式，鼠标悬停即可【预览】样式。
3.  点击【＋】可以添加本地引用样式  
    

![](https://pic1.zhimg.com/v2-fb445fbf5356e32be94e6b6652191d14_r.jpg)![](https://pic4.zhimg.com/v2-c3267a7f7eed42ee21268c86707905e7_r.jpg)

*   【搜索】：建议保持不变
*   【导出】：根据自己需求更改【默认格式】 选中条目使用快捷键【Cmd+Shift+C】可以【便捷复制】默认引用样式
*   【高级】：建议保持不变，可更改 Zotero【数据存储位置】和查看【快捷键】

### **2.2.2 插件：Zotero 插件环境配置**

### **2.2.2.1** [ZotFile](https://link.zhihu.com/?target=http%3A//zotfile.com/)

*   功能

1.  自动修改附件名
2.  提取附件中的笔记
3.  【Attaching New Files】—添加新附件
4.  【Send to Tablet】—多端同步阅读

*   环境配置

点击【工具】—进入【Zotfile Preferences】

*   【General Settings】

*   【Source Folder For Attaching New Files】：自动抓取新附件 建议设置为【默认下载地址】
*   【Location of Files】：附件本地存储地址 建议选择【Attach stored copy of files(s)】，存储在 Zotero 的根目录下

![](https://pic3.zhimg.com/v2-c561d9d6a8167438ed94ca1ad613c1e2_r.jpg)

*   【Send to Tablet】：若非本地存储空间不够，不建议使用  
    具体设置可参考  
    

*   [青柠学术 - Zotero + Tablet，跨平台文献同步的新姿势！](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/uHOY2a_EZqJAQOrB2v9rFQ)

![](https://pic4.zhimg.com/v2-c1d54ce2a202f49c2b001c256be9902b_r.jpg)

*   【Renaming Rules】和【Advanced Settings】：可自行修改

### **2.2.2.2** [ZoteroQuickLook](https://link.zhihu.com/?target=https%3A//github.com/mronkko/ZoteroQuickLook/releases)

Zotero6 请安装此版本【[ZoteroQuickLookReload](https://link.zhihu.com/?target=https%3A//github.com/404neko/ZoteroQuickLookReload)】

[ZoteroQuickLookReload](https://link.zhihu.com/?target=https%3A//github.com/404neko/ZoteroQuickLookReload)

1.  下载【QuickLook】本体

*   Mac：即系统提供的【预览】功能
*   Windows：[QuickLook for Windows](https://link.zhihu.com/?target=https%3A//github.com/QL-Win/QuickLook) 文件见网盘

2. 下载【[ZoteroQuickLook](https://link.zhihu.com/?target=https%3A//github.com/mronkko/ZoteroQuickLook/)】

*   功能： 按【空格】实现快速预览

### **2.2.2.3** [茉莉花 - Jasminum](https://link.zhihu.com/?target=https%3A//github.com/l0o0/jasminum)

*   功能：

1.  拆分或合并 Zotero 中条目作者姓和名
2.  根据知网上下载的文献文件来抓取引用信息（根据文件名）
3.  添加中文 PDF/CAJ 时，自动拉取知网数据，该功能默认关闭。需要到设置中开启，注意添加的文件名需要含有中文，全英文没有效果（根据文件名）
4.  为知网的学位论文 PDF 添加书签
5.  更新中文翻译器

*   2021.1.25 更新的 v0.0.9：添加不同系统下 pdftk 的默认目录，默认安装时**不必再**手动选择目录。如默认目录无法识别，请按照下列步骤手动操作。  
    
*   如何自动为知网学位论文添加【书签】

从知网下载的 PDF 格式【学位论文】不显示书签（CAJ 格式显示），【茉莉花】提供自动添加功能。 要使用添加【书签】功能需要下载【PDFtk Server】，文件见网盘。

1.  下载并安装【PDFtk Server】
2.  打开【Zotero】—进入【首选项】—进入【茉莉花】 选择【PDFtk Server】的路径，最后须选择`bin`确认 Mac 可以使用快捷键`Shift+Command+G`，输入路径`/opt/pdflabs/pdftk/`

![](https://pic4.zhimg.com/v2-45d800a67ed65cb8f831cc8252c8f577_r.jpg)

*   更新中文翻译器

1.  点击【刷新】—【更新全部】
2.  更新【Zotero Connector】，具体参见 2.1.3

![](https://pic2.zhimg.com/v2-4d4a829520d1c92d058c703d77526601_r.jpg)

### **2.2.3 移动端：多平台同步阅读环境配置**

具体操作与 2.2.1 中【WebDAV】设置相同

*   iPadOS：【Papership【绑定 Zotero 账号 + WebDav  
    

*   可参考 [青柠学术 - 详解【Zotero+PaperShip + 坚果云】文献生态的同步机制！](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s%3F__biz%3DMzAxNzgyMDg0MQ%3D%3D%26mid%3D2650456887%26idx%3D2%26sn%3Df33a0a4461ee915e1c8f9880066cab68%26chksm%3D83d1def1b4a657e7d9d7c18062dbb1977725e9a891294b686379311d71d9fcf1beac81e168bb%26scene%3D178%26cur_album_id%3D1319074508795641857%23rd)

*   Android：【Zoo for Zotero】绑定 Zotero 账号 + WebDav  
    

*   可参考 [青柠学术 - Zoo for Zotero，安卓上阅读 Zotero 文献的利器！](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s%3F__biz%3DMzAxNzgyMDg0MQ%3D%3D%26mid%3D2650456795%26idx%3D2%26sn%3D2060a39b9ed6798c1990aa72765c637e%26chksm%3D83d1df1db4a6560b76ee330c13a917027b271ce9e61bb8aad31cf28bbbb0e95459763b67af63%26scene%3D178%26cur_album_id%3D1319074508795641857%23rd)

### **2.2.4 搜索引擎：搜索引擎环境配置**

1.  进入 Zotero 根目录下`/locate`位置 可进入【首选项】—【高级】—【文件和文件夹】—【打开数据文件夹】进入 Zotero 根目录
2.  用网盘中的【engines.json】替换【locate】中的文件

![](https://pic1.zhimg.com/v2-10f99b781d591d477ccd3d3e9ad38054_r.jpg)

由于网盘被封禁，将代码粘贴在这里：

```
[
	{
		"_name": "CNKI新版",
		"_alias": "CNKI",
		"_description": "CNKI新版",
		"_icon": "http://kns8.cnki.net/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://kns8.cnki.net/kns/DefaultResult/Index?dbcode=SCDB&kw={z:title}&korder=SU",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "http://kns8.cnki.net/favicon.ico"
	},
	{
		"_name": "南京师范大学图书馆",
		"_alias": "南京师范大学图书馆",
		"_description": "南京师范大学图书馆",
		"_icon": "http://lib.njnu.edu.cn/images/njnulogo.png",
		"_hidden": false,
		"_urlTemplate": "http://opac.njnu.edu.cn/opac/openlink.php?strSearchType=title&match_flag=forward&historyCount=1&strText={z:title}&doctype=ALL&with_ebook=on&displaypg=20&showmode=list&sort=CATA_DATE&orderby=desc&location=ALL&csrf_token=%29lW1vOCx%7B%2F",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "http://lib.njnu.edu.cn/images/njnulogo.png"
	},
		{
		"_name": "豆瓣读书",
		"_alias": "豆瓣读书",
		"_description": "豆瓣读书",
		"_icon": "https://book.douban.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://search.douban.com/book/subject_search?search_text={z:title}&cat=1001",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://book.douban.com/favicon.ico"
	},		
		{
		"_name": "国学数典",
		"_alias": "国学数典",
		"_description": "国学数典",
		"_icon": "https://bbs.ugxsd.com/static/image/common/logo_gxsd.png",
		"_hidden": false,
		"_urlTemplate": "https://bbs.ugxsd.com/search.php?mod=forum&searchid=2634&orderby=lastpost&ascdesc=desc&searchsubmit=yes&kw={z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://bbs.ugxsd.com/static/image/common/logo_gxsd.png"
	},		
		{
		"_name": "读秀图书",
		"_alias": "读秀图书",
		"_description": "读秀图书",
		"_icon": "https://book.duxiu.com/images/small0408.jpg",
		"_hidden": false,
		"_urlTemplate": "https://book.duxiu.com/search?Field=all&channel=search&sw={z:title}&ecode=utf-8&edtype=&searchtype=&view=0",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://book.duxiu.com/images/small0408.jpg"
	},
	{
		"_name": "Obsidian",
		"_alias": "Obsidian",
		"_description": "在Obsidian中搜索",
		"_icon": "https://obsidian.md/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "obsidian://search?vault=Zotero&query={z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://obsidian.md/favicon.ico"
	},	
	{
		"_name": "Open Notes",
		"_alias": "Open Notes",
		"_description": "笔记路径放在Rights字段",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017133213.png",
		"_hidden": false,
		"_urlTemplate": "file:///{z:rights}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017133213.png"
	},
		{
		"_name": "TOC of Notes",
		"_alias": "TOC of Notes",
		"_description": "打开所有笔记的目录",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201025110921.png",
		"_hidden": false,
		"_urlTemplate": "file:////Users/a40781/Zotero/Obsidian",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201025110921.png"
	},
		{
		"_name": "N-Connected Papers",
		"_alias": "Connected Papers文献网络",
		"_description": "Connected Papers文献网络",
		"_icon": "https://www.connectedpapers.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://www.connectedpapers.com/search?q={z:title}+{z:year}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://www.connectedpapers.com/favicon.ico"
	},
	{
		"_name": "CrossRef",
		"_alias": "CrossRef",
		"_description": "CrossRef Search",
		"_icon": "https://www.crossref.org/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://crossref.org/openurl?{z:openURL}&pid=zter:zter321",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "http://crossref.org/favicon.ico"
	},
	{
		"_name": "Google Scholar",
		"_alias": "Google Scholar",
		"_description": "Google Scholar Search",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016230633.png",
		"_hidden": false,
		"_urlTemplate": "http://scholar.google.com/scholar?as_q=&as_epq={z:title}&as_occt=title&as_sauthors={rft:aufirst?}+{rft:aulast?}&as_ylo={z:year?}&as_yhi={z:year?}&as_sdt=1.&as_sdtp=on&as_sdtf=&as_sdts=22&",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016230633.png"
	},
	{
		"_name": "Google Scholar - Title Only",
		"_alias": "Google Scholar",
		"_description": "Google Scholar Search - Title Only",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016230633.png",
		"_hidden": false,
		"_urlTemplate": "http://scholar.google.com/scholar?as_q=&as_epq={z:title}&as_occt=title&as_sdt=1.&as_sdtp=on&as_sdtf=&as_sdts=22&",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016230633.png"
	},
		{
		"_name": "Google Patent",
		"_alias": "Google Scholar",
		"_description": "Google Patent - Search",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017210030.png",
		"_hidden": false,
		"_urlTemplate": "https://patents.google.com/?q=({z:title})&oq=({z:title})",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017210030.png"
	},
		{
		"_name": "Semantic Scholar - DOI",
		"_alias": "Semantic Scholar",
		"_description": "Semantic Scholar",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017165044.png",
		"_hidden": false,
		"_urlTemplate": "https://api.semanticscholar.org/{z:DOI}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017165044.png"
	},
	{
		"_name": "Google",
		"_alias": "Google",
		"_description": "Google Search",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016230909.png",
		"_hidden": false,
		"_urlTemplate": "https://www.google.com/#q={z:title}+{rft:aufirst?}+{rft:aulast?}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016230909.png"
	},
	{
		"_name": "Web of Science",
		"_alias": "WOS",
		"_description": "Web of Science Search",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016231207.png",
		"_hidden": false,
		"_urlTemplate": "http://ws.isiknowledge.com/cps/openurl/service?url_ver=Z39.88-2004&{z:openURL}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016231207.png"
	},
	{
		"_name": "WOS Citing Articles",
		"_alias": "WOS Citing Articles",
		"_description": "Web of Science Citing Articles Search",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016231207.png",
		"_hidden": false,
		"_urlTemplate": "http://ws.isiknowledge.com/cps/openurl/service?url_ver=Z39.88-2004&svc_val_fmt=info:ofi/fmt:kev:mtx:sch_svc&svc.citing=yes&{z:openURL}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016231207.png"
	},
	{
		"_name": "WOS Related Articles",
		"_alias": "WOS Related Articles",
		"_description": "Web of Science Related Articles Search",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016231207.png",
		"_hidden": false,
		"_urlTemplate": "http://ws.isiknowledge.com/cps/openurl/service?url_ver=Z39.88-2004&svc_val_fmt=info:ofi/fmt:kev:mtx:sch_svc&svc.related=yes&{z:openURL}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016231207.png"
	},
	{
		"_name": "Sci-Hub DOI",
		"_alias": "Sci-Hub DOI",
		"_description": "SciHub Lookup Lookup",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200912.png",
		"_hidden": false,
		"_urlTemplate": "http://sci-hub.shop/{z:DOI}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200912.png"
	},
	{
		"_name": "Sci-Hub URL",
		"_alias": "Sci-Hub URL",
		"_description": "SciHub URL Lookup",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200912.png",
		"_hidden": false,
		"_urlTemplate": "http://sci-hub.shop/{z:url}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200912.png"
	},
			{
		"_name": "Sci-Hub最新网址",
		"_alias": "Sci-Hub最新网址",
		"_description": "Sci-Hub最新网址",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200912.png",
		"_hidden": false,
		"_urlTemplate": "https://iseex.github.io/scihub/",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200912.png"
	},
		{
		"_name": "Connected Papers（手动输入doi）",
		"_alias": "Connected Papers文献网络",
		"_description": "Connected Papers文献网络",
		"_icon": "https://www.connectedpapers.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://www.connectedpapers.com",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://www.connectedpapers.com/favicon.ico"
	},
		{
		"_name": "Connected Papers（Title Only）",
		"_alias": "Connected Papers文献网络",
		"_description": "Connected Papers文献网络",
		"_icon": "https://www.connectedpapers.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://www.connectedpapers.com/search?q={z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://www.connectedpapers.com/favicon.ico"
	},
		{
		"_name": "iJournal期刊影响因子（首选1）",
		"_alias": "iJournal期刊影响因子",
		"_description": "期刊影响因子查询（仅支持搜索ISSN）",
		"_icon": "https://ijournal.topeditsci.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://ijournal.topeditsci.com/search?keywordType=title&keyword={rft:jtitle}&ifStart2019=&ifEnd2019=&jcr=&sub=&isDomestic=&selfCitingRate=all&compatriotRate=all&totalReviewRatio=all&categoryId=&pageNum=1&order=&orderType=",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://ijournal.topeditsci.com/favicon.ico"
	},
		{
		"_name": "JustScience影响因子（首选2）",
		"_alias": "JustScience期刊影响因子（首选2）",
		"_description": "JustScience期刊影响因子（首选2）",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017105103.png",
		"_hidden": false,
		"_urlTemplate": "https://sci.justscience.cn/index.php?q={rft:jtitle}&sci=1",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017105103.png"
	},
		{
		"_name": "中文期刊搜索",
		"_alias": "中文期刊搜索",
		"_description": "JustScience中文期刊搜索",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017105103.png",
		"_hidden": false,
		"_urlTemplate": "https://sci.justscience.cn/index.php?q={rft:jtitle}&sci=0",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201017105103.png"
	},
		{
		"_name": "Letpub期刊搜索",
		"_alias": "Letpub期刊搜索",
		"_description": "Letpub期刊搜索（仅支持搜索ISSN）",
		"_icon": "https://www.letpub.com.cn/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://www.letpub.com.cn/index.php?page=journalapp&view=search&searchname={rft:jtitle}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://www.letpub.com.cn/favicon.ico"
	},
		{
		"_name": "期刊影响因子查询",
		"_alias": "期刊影响因子查询",
		"_description": "期刊影响因子查询（仅支持搜索ISSN）",
		"_icon": "https://www.xueky.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://www.xueky.com/rank.php?qk={rft:jtitle}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://www.xueky.com/favicon.ico"
	},
			{
		"_name": "期刊近五年影响因子",
		"_alias": "期刊近五年影响因子",
		"_description": "期刊近五年影响因子",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200307.png",
		"_hidden": false,
		"_urlTemplate": "http://www.greensci.net/search?kw={rft:jtitle}",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016200307.png"
	},
		{
		"_name": "Unpaywall",
		"_alias": "Unpaywall",
		"_description": "Unpaywall Lookup",
		"_icon": "https://oadoi.org/static/img/favicon.png",
		"_hidden": false,
		"_urlTemplate": "https://oadoi.org/{z:DOI}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://oadoi.org/static/img/favicon.png"
	},
		{
		"_name": "LibGen",
		"_alias": "LibGen",
		"_description": "Look up books on Library Genesis",
		"_icon": "http://gen.lib.rus.ec/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://gen.lib.rus.ec/search.php?req={rft:aufirst?}+{rft:aulast?}+{rft:title?}+{z:ISBN?}",
		"_urlParams": [],
		"_method": "GET",
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:book",
			"xmlns": "http://a9.com/-/spec/opensearch/1.1/",
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "http://gen.lib.rus.ec/favicon.ico"
	},
		{
		"_name": "Wikipedia",
		"_alias": "Wikipedia",
		"_description": "Wikipedia",
		"_icon": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016232045.png",
		"_hidden": false,
		"_urlTemplate": "https://zh.wikipedia.org/wiki/{z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://figurebed-iseex.oss-cn-hangzhou.aliyuncs.com/img/20201016232045.png"
	},
	{
		"_name": "ProQuest",
		"_alias": "ProQuest",
		"_description": "ProQuest Search",
		"_icon": "https://www.proquest.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://proquest.umi.com/pqdweb?SQ=TI(+{z:title}+)+YR(+{z:year?}+)&RQT=305&querySyntax=PQ&searchInterface=1&moreOptState=CLOSED&TS=1139706667&JSEnabled=1&DBId=-1",
		"_urlParams": [],
		"_urlNamespaces": {
			"rft": "info:ofi/fmt:kev:mtx:journal",
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "http://www.proquest.com/favicon.ico"
	},
			{
		"_name": "Zlibrary Book",
		"_alias": "Zlibrary Book",
		"_description": "Zlibrary Book",
		"_icon": "https://z-lib.org/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://b-ok.cc/s/{z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://z-lib.org/favicon.ico"
	},
		{
		"_name": "Zlibrary Articles",
		"_alias": "Zlibrary Articles",
		"_description": "Zlibrary Articles",
		"_icon": "https://z-lib.org/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://booksc.xyz/s/{z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://z-lib.org/favicon.ico"
	},
		{
		"_name": "SooPAT专利搜索",
		"_alias": "SooPAT专利搜索",
		"_description": "SooPAT专利搜索",
		"_icon": "http://www.soopat.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://www.soopat.com/Home/Result?SearchWord={z:title}&FMZL=Y&SYXX=Y&WGZL=Y&FMSQ=Y",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "http://www.soopat.com/favicon.ico"
	},
	{
		"_name": "百度学术搜索",
		"_alias": "BaiDu",
		"_description": "百度学术搜索",
		"_icon": "http://xueshu.baidu.com/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://xueshu.baidu.com/s?wd={z:title}&rsv_bp=0&tn=SE_baiduxueshu_c1gjeupa&rsv_spt=3&ie=utf-8&f=8&rsv_sug2=0&sc_f_para=sc_tasktype%3D%7BfirstSimpleSearch%7D",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "http://xueshu.baidu.com/favicon.ico"
	},
			{
		"_name": "万方搜索",
		"_alias": "万方搜索",
		"_description": "万方搜索",
		"_icon": "http://www.wanfangdata.com.cn/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "http://www.wanfangdata.com.cn/search/searchList.do?searchType=all&showType=&pageSize=&searchWord={z:title}&isTriggerTag=",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "http://www.wanfangdata.com.cn/favicon.ico"
	},
	{
		"_name": "谷粉学术",
		"_alias": "谷粉学术",
		"_description": "谷粉学术",
		"_icon": "https://img.99lb.net/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://cc.gufenxueshu.com/scholar?q={z:title}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://img.99lb.net/favicon.ico"
	},
		{
		"_name": "Glgoo学术",
		"_alias": "Glgoo学术",
		"_description": "Glgoo学术",
		"_icon": "https://xue.glgoo.org/favicon.ico",
		"_hidden": false,
		"_urlTemplate": "https://xue.xiayige.org/scholar?hl=zh-CN&q={z:title}&btnG=&lr=",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#",
			"": "http://a9.com/-/spec/opensearch/1.1/"
		},
		"_iconSourceURI": "https://xue.glgoo.org/favicon.ico"
	}
]

```

### **2.2.5 RSS：订阅环境配置**

*   获取 RSS 源

*   [知网期刊](https://link.zhihu.com/?target=https%3A//navi.cnki.net/KNavi/Journal.html) 进入待添加期刊页面，点击【RSS 订阅】，跳出网页的【URL】即为该期刊的 RSS 订阅地址
*   [青柠学术 - Zotero｜推荐几个非常不错的 Rss 订阅源](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s%3F__biz%3DMzAxNzgyMDg0MQ%3D%3D%26mid%3D2650457597%26idx%3D1%26sn%3D6ea1d954f5b9fe036f0565ed98df4f08%26chksm%3D83d1d83bb4a6512d2d266548745e3524107dbf327049a23c53adc9d539c0f794f299602044da%26scene%3D178%26cur_album_id%3D1319074508795641857%23rd)

*   下载【Tampermonkey】浏览器插件 ，文件见**网盘**

*   安装插件 [RSS+ : 显示当前网站所有的 RSS](https://link.zhihu.com/?target=https%3A//greasyfork.org/zh-CN/scripts/373252-rss-show-site-all-rss)
*   点击网页右下角圆点即可获取 RSS 源

![](https://pic2.zhimg.com/v2-81038443fc80c40ebb3c9c8b3b123721_r.jpg)

*   添加 RSS 源 打开【Zotero】—点击左上第二个文件夹 图标——新建【订阅】—来自【URL…】

![](https://pic4.zhimg.com/v2-7c6ea051da121db88596b1652e99c7d7_r.jpg)

3 应用
----

### **3.1 工作流：以 Zotero 为中枢**

![](https://pic1.zhimg.com/v2-aeb24d29d141718181e44809ed2650b8_r.jpg)

*   检索 / 阅读 / 笔记

*   确定题目 / 开题报告 / 文献综述

*   下载论文——Zotero 抓取
*   可视化文献处理——Zotero 存储 bib，导出处理
*   多端同步阅读——移动端同步 Zotero 账号

*   存档 & 归类——Zotero 文件夹分类以及 Tag 分类
*   文献笔记——与 Zotero 条目联结

*   写作

*   插入引文生成参考文献——Zotero 通过文字处理软件插件插入参考文献
*   调整格式——修改 Zotero 参考文献引用格式设置

*   回溯

*   用 Zotero 搭建自己的知识库

### **3.2 下载论文**

*   正着下：抓取  
    

*   单篇

![](https://pic1.zhimg.com/v2-ffb53b1ba5b27fff8e5dd3993bd92460_r.jpg)

*   批量

![](https://pic4.zhimg.com/v2-68f4036b18315d0080c6df89bc3e38d7_r.jpg)

*   反着下  
    

*   识别：从文献到题录

英文文献会自动抓取元数据，若失败请点【重新抓取 PDF 的元数据】

![](https://pic4.zhimg.com/v2-6b839153248c39319a7855200e7b8f8f_r.jpg)

*   检索：从题录到文献

![](https://pic3.zhimg.com/v2-98cfb7b3e0d3b8f382096fdd5794112e_r.jpg)

### **3.3 储存 & 分类**

### **3.3.1 新建分类**

![](https://pic4.zhimg.com/v2-80f8044b365436df91218162c482f85f_r.jpg)

### **3.3.2 Tag 管理**

*   添加 Tag

![](https://pic4.zhimg.com/v2-916d341bf9f98fc26f87aa29310781df_r.jpg)

*   给 Tag 添加颜色

![](https://pic2.zhimg.com/v2-14a2d14760e611f7450f2bab9c5e4551_r.jpg)

*   检索 Tag：单击左下角【Tag 区】中的 Tag

### **3.3.3 高级检索**

![](https://pic2.zhimg.com/v2-711cc405cd5a494c55ebce650fb93fb5_r.jpg)

### **3.4 阅读**

### **3.4.1 导出 PDF 批注**

![](https://pic4.zhimg.com/v2-47fa9f5b2456ba5fbe191aa1f691b9f7_r.jpg)

### **3.4.2 联结文献笔记**

### **3.5 写作**

### **3.5.1 插入参考文献**

![](https://pic1.zhimg.com/v2-50fad20bbc77693a1a3024523c006454_r.jpg)

### **3.6 分享**

### **3.6.1 导出条目及附件**

![](https://pic4.zhimg.com/v2-6269642cd44d0d11291c8cb6069a0e4f_r.jpg)

**3.6 分享**
----------

### **3.6.1 导出条目及附件**

![](https://pic4.zhimg.com/v2-6269642cd44d0d11291c8cb6069a0e4f_r.jpg)

### **3.6.2 团队协作**

![](https://pic2.zhimg.com/v2-5bae80ba1fb0e04aa2e118706b009055_r.jpg)![](https://pic4.zhimg.com/v2-d536855bca040fb148b205bcc7261cb7_r.jpg)

如果对我感兴趣的话，可以扫描二维码关注我的**公众号** “一圆堂”。