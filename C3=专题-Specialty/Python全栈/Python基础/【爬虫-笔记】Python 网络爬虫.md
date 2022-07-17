#pending #project #area/cs #area/ot/python 
# 1 初识网络爬虫
## 1.1 分类
* 通用网络爬虫
* 聚焦网络爬虫
* 增量式网络爬虫
* 深层网络爬虫
## 1.2 基本原理
1. 获取初识URL
2. 爬取页面获取新的URL
3. 将新的URL放到URL队列中
4. 读取新的URL下载网页
5. 重复上述爬取过程（2、3、4）直到满足停止条件
## 1.3 环境搭建
1. Anaconda（Python3）
2. Pycharm

# 2 了解Web前端
HTML 定义网页的内容
CSS 描述网页的样式
JavaScript 描述网页的行为
## 2.1 HTTP基本原理
**HTTP**：超文本传输协议
建立链接-请求-应答-关闭连接
### 常用请求方式
**GET**：指定页面
**POST**：提交数据、处理请求
**HEAD**：获取报文头部信息
**PUT**：传送数据，替代文档内容
**DELETE**：请求服务器删除指定页面
**OPTION**：允许客户端查看服务器内容
### HTTP状态码及其含义
1** 信息
2** 成功
3** 重定向
4** 客户端错误
5** 服务器错误

## 2.2 HTML语言
### 结构
文档类型
```html
<!DOCTYPE html>
```
根标签
```html
<html lang="en">
```
头标签
```html
<head>
	<meta charset="UTF-8">
	<title>在网页中插入图片</title>
</head>
```
主体标签
```html
<body>
<img src="mr.png" width="400" height="400">
</body>
```
### HTML的基本标签
1. 文件开始标签html
2. 文件头部标签head
3. 文件标题标签title
4. 元信息标签meta
5. 页面主体标签body
#### body标签的属性及其描述
| 属性         | 描述                                           |
| ------------ | ---------------------------------------------- |
| text         | 设定页面文字的颜色                             |
| bgcolor      | 设定页面背景的颜色                             |
| background   | 设定页面背景的图像                             |
| bgproperties | 设定页面背景的图像为固定，不随页面的滚动而滚动 |
| link         | 设定页面默认的连接颜色                                               |
| alink        | 设定鼠标正在点击时的连接颜色                                               |
| vlink        | 设定访问过后的连接颜色                        |
| topmargin    | 设定页面的上边距                                              |
| leftmargin   | 设定页面的左边距                                 |


## 2.3 CSS层叠样式表
### 属性选择器
p标签
```html
[att=val]{}
```
### 类和ID选择器
```html
	#intro{color}   <!---ID选择器 只能定义一个--->
	.intro{color}   <!---类选择器 需要用class属性来声明--->
```

## 2.4 JavaScript动态脚本语言
### 在页面中直接链接JavaScript代码
```html
<script>···</script>
```
属性值：
| 属性值   | 说明                                           |
| -------- | ---------------------------------------------- |
| language | 设置所使用的脚本语言及版本                     |
| src      | 设置一个外部脚本文件的路径位置                 |
| type     | 设置所使用的脚本语言，此属性已代替language语言 |
| defer    | 当HTML文档加载完毕后再执行脚本语言                                               |
链接外部JavaScript文件
```html
<script language="javascript" src="your-Javascript.js">···</script>
```
# 3 请求模块 Urllib
## Urllib简介
urllib.request:实现基本的HTTP请求的模块
urllib.error:异常处理模块
urllib.parse:用于解析URL的模块
urllib.robotparser:用于解析robots.txt文件，判断网站是否可以爬取信息
## 使用urlopen()方法发送请求
```python
urllib.request.uropen(url,data=None,[timeout,]*,cafile=None,capath=None,cadefault=False.context=None)
```