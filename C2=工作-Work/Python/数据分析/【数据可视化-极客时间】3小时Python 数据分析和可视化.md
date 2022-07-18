# 3小时Python 数据分析和可视化
#area/cs #area/ot/python #end
1. 分解问题

2. 数据分析

3. Python实现

4. 总结经验

## 01 课程目标

1. 掌握分解问题的能力
2. 学会用Python进行数据处理、分析、展示
3. 总结经验

## 02 确定目标

​	**问题特点：主观性$\longrightarrow$​客观性**

​	example： 

​	冷不冷？$\longrightarrow$（数值化）温度、湿度、温度变化、同期变化特点......

​	**界定**

​	简单问题还是复杂问题

​		简单问题：数据分析

​		复杂问题：机器学习

## 03 问题分解

example：赛博朋克香不香？

问题分解：
	金钱成本（购买游戏、升级硬件）

​	时间成本

​	$\cdots$

## 04 代码实现·数据数据收集

1. 收集哪类用户数据
2. 收集哪类数据
3. 主观还是客观数据

example：豆瓣《赛博朋克2077》评分页面

jupyter notebook运行代码

**模拟浏览器**

​	**HTTP协议**（学习后端开发的第一个山坡——协议）

  - 请求行

    ```python
    GET /xxx.html HTTP/1.1 (CRLG)
    #请求方法 URI	协议版本	换行
    ```

  - 请求头

    浏览器F12 Request Hearders

  - 请求报文

**代码**

```python
#获取完整网页 豆瓣评论区，NetWork ctrl+R

import requests
r=requests.get('https://www.douban.com/game/25931998/comments?state=20$sort=score')

#看结果具体信息
print(r.status_code)	##418	#返回的状态码
print(r.text)

#获取请求头
url= 'https://www.douban.com/game/25931998/comments?state=20$sort=score'
my_headers = ('user-agent':'ozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.131 Safari/537.36')	#字典
r =requests.get(url,headers=my_headers)

print(r.status_code)	##200
#网页内容
print(r,text)
```

```python
#获取网页指定内容

import requests
url= 'https://www.douban.com/game/25931998/comments?state=20$sort=score'
my_headers = ('user-agent':'ozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.131 Safari/537.36')	#字典
r =requests.get(url,headers=my_headers)

#r.text网页完整内容。提取有用的数据
#需pip install lxml
#转化为能被XPath匹配的格式
from lxml import etree
selector=etree.HTML(r.text)
#取出对象后继续匹配 Element通过标签区分
#ctrl+F //div任意div
selector.xpath('//div[@class="user-info"]')

#获取用户名
username = selector.xpath('//div[@class="user-info"]/a/text()')	#豆瓣中的a标签是用户名
print(username)
len（username）	##20
#获取打星(第二个span标签)
star=selector.xpath('//div[@class="user-info"]/span[2]/@class')	#@class获取属性值
print(star)
len(star)		##<=20
#获取评论
comment=selector.xpath('//span[@class="short"]/text()')
print(comment)
len(comment)

##处理星级(用户和星级关联)——小观
temp=selector.xpath('//div[@class="user-info"]')	#取得中间结果
#temp[0]	#序列切分
#if not temp[0].xpath('.span[2]/@class'):
#    print('allstar0')

#泛化（用户星级一一对应）
for everyElement in temp:
    username=everyElement.xpath('./a/text()')
    star=everyElement.xpath('./span[2]/@class')
    if not star:
        star=[]
        star.append("allstar0")
        print(f"{username}::{star}") 
#继续处理评论
temp=selector.xpath('//div[@class="info"]')
	#迭代每一个元素
for everyElement in temp:
    username=everyElement.xpath('./a/text()')
    star=everyElement.xpath('./span[2]/@class')
    if not star:
        star=[]
        star.append("allstar0")
	comment=everyElement.xpath('./p/span[@class="short"]/text()')
    game_short=f"{username}::{star}::{comment}=="
    
#保存到文件做持久化存储
#继续处理评论
temp=selector.xpath('//div[@class="info"]')
#以追加写入方式打开文件
with open("./game_short.txt","w+") as f:
    for everyElement in temp:
        username=everyElement.xpath('./a/text()')
        star=everyElement.xpath('./span[2]/@class')
        if not star:
            star=[]
            star.append("allstar0")
        comment=everyElement.xpath('./p/span[@class="short"]/text()')
        game_short=f"{username}::{star}::{comment}=="
        f.write(game_short)
        
#问题的延伸
#1. 怎么翻页？
#2. 怎么确定是最后一页？
#问题延伸的延伸
#1. 怎么让代码更容易被读懂？
#2. 更复杂的需求如何解决？	#更多网站去采集
```

> **DAY1**
>
> 思考：
>
> ​	数据收集中面对了哪些问题？如何解决的？
>
> 结论：
> 	1. 问题需要分解到你能够解决的领域
>  	2. 协议、框架是开发能力的体现
>  	3. 基础语法是分解问题的最小单元
>  	4. 简单的编程语言有助于聚焦问题本身
>  	5. 语言是思维的工具
>  	6. 学习哪一种语言不重要

## 05 数据存储与处理

### 5.1 数据存储

- 存储什么介质

- 存储在什么软件

- 存储在什么架构

### 5.2 数据清洗

- 冗余数据
- 缺失数据
- 异常数据

### 5.3 数据预处理

80%格式	后续处理效率的主要影响因素

10%编码	乱码导致结果误差

10%数据组合和拆分	做到并发和一致性

### 5.4 正则表达式

**应用场景**

1. 验证
2. 模糊查找
3. 模式替换

**常用元字符**

| 元字符 | 功能性质                             |
| ------ | ------------------------------------ |
| .      | 除了换行符（\n）以外的单个字符       |
| '      | 字符串的开头                         |
| $      | 字符串的结尾                         |
| *      | *前面多个重复字符，包含0个           |
| +      | +前面多个重复字符，不包含0个         |
| ？     | ？前面字符出现0或1次                 |
| {n}    | 前面字符出现n次，{m,n}表示出现m到n次 |
| \      | 转义字符                             |

```python
# 正则表达式
#Python使用re模块进行文本模式匹配
#re是标准库，不需要安装
import re
pattern = 'something'
string = 'something'
prog = re.compile(pattern)
result = prog.match(string)
print(result)	#<re.Match<re.Match object; span=(0, 9), match='something'>
```

```python
import re

pattern = 's.*g'
string1='something'
string2='sisviluiog'
string3='shggjdskg'
prog=re.compile(pattern)
result1=prog.match(string1)
result2=prog.match(string2)
result3=prog.match(string3)
print(result1)	#print(result)	#<re.Match<re.Match object; span=(0, 9), match='something'>
print(result2)  #<re.Match object; span=(0, 10), match='sisviluiog'>
print(result3)  #<re.Match object; span=(0, 9), match='shggjdskg'>
```

```python
#网址正则匹配
re.match('.*@.*.com','123@123.com')
#分组
re.match('(.*)@(.*\.com)','xyz@123.com').group(1)	'xyz'
re.match('(.*)@(.*\.com)','123@123.com').group(1)	'123.com'
```

```python
#用正则表达式的5个常用函数
#re.match()
#re.search()	#返回第一个成功匹配的字符串
#re.findall
#re.sub()
#re.split()
#用正则表达式调整文本内容
with open(''./game_short.txt','r') as f:
          #读取文本一行
          comment=f.readline()
print(comment)
#尝试用替换调整文本的内容
import re
temp_comment=re.sub('==','\n',comment)
print(comment) #一行的文件以“==”（不含）分开

type(temp_comment)	#str
re.split('==',comment)[0]
re.split('==',comment)[0].split('::')
          
#使用正则表达式处理格式
result=[]
for line in re.split("==",comment):
      result.append(line.split('::'))
print(result)
#使用正则表达式清洗内容
          #allstar10→10
temp = re.split('==',comment)[0]
print(temp)
		#一些[和’是正文里面的内容，需转义，{1,2}表示前面[]里的内容出现一次或两次
        #每对（）为一个分组，\1为第一对（）中的内容
re.sub('\[\'allstar([0-9]{1,2})\'\]',r'***\1***',comment)
```

### 5.5 数据处理

```python
#提取所有的分数和评论各自放在一个列表中
import re
with open('./game_shory=t.txt','r') as f:
    comment = f.readline()
star = re.sub('\[\'allstar([0-9]{1,2})\'\].*?==',r'\1',comment)
star_list = re.split(',',star)
print(star_list)
comment_list=[]
comment_line = re.split(r'::',comment)
for line in comment_line:
    if re.search('==',line):
        comment_context = re.split('==',line)[0]
        comment_list.append(re.sub('\[\'(.*)\'\]',comment_context))
print(comment_list)

#统计重复分值个数
from collection import Counter
result=Counter(star_list)
print(result)
##注意要补充0个的情况
list1=[ result[i] for i in sorted(result)]
#list1=[]
#for i in sorted(result):
#	list1.append(result[i])

#柱状图
from pyecharts.charts import Bar
bar=Bar()	#实例化
bar.add_xaxis(["0分","10分","20分","30分","40分"，"50分"])
bar.add_yaxis("赛博朋克2077"，[result[i] for i insorted(result)])
bar.render_notebook()
#bar.render("mycharts.html")	#渲染成网页

#饼图
from pyecharts.charts import Pie
attr=["0分","10分","20分","30分","40分"，"50分"]
values=[result[i] for i insorted(result)]
pir=Pie()
pie.add("",[z for z in zip(attr.values)])
pie.render_notebook()
```

```python
#jieba分词
import jieba
my_comment='这东西好'
#分词
seg_list=jieba.cut(my_comment)
print("/".join(seg_list))	##这/东西/好
#动态添加词组
jieba.add_word('东西好')
seg_list=jieba.cut(my_comment)
print("//".join(seg_list))	##这//东西好
jieba.del_word('东西好')

#提取关键词
import jieba
import jieba.analyse
#关键词筛选
	#增加停止词
jieba.analyse.set_stop_words("./stop_words.txt")
topK=10
result=','.join(comment_list)
tags=jieba.analyse.extract_tags(result,topK=topK,allowPOS=())
top10=",".join(tags)
print(top10)
tags2=jieba,analyse.extract_tags(result,topK=topK,withWeight=True,allowPOS=('v','vn','n'))	#权重，词性筛选
print(tags2)

#生成词云
from pyecharts import options as opts
from pyecharts.charts import WordCloud
from pyecharts.globals import SymbolType
wordcloud = WordCloud()
wordcloud.add("",tags,word_size_range=[20,100],shape=SymbolType.DIAMOND)
wordcloud.render_notebook()
```

可视化 pyecharts

总结：

1. 正则表达式可以按照模式灵活匹配

2. Echarts是通用组件，可以前后端分离
3. 中文分词要比英文分词考虑的问题更多
4. 好的词库是分词的关键
