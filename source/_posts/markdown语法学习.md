---
title: Markdown语法学习
id: 100
categories:
- [笔记,Markdown]
date: 2016.11.12
tags: 
---

# Markdown语法学习
这里介绍是Markdown的一些基本语法，方便大家学习。

最后编辑：2016.12.14
修改了页面中的部分不规范语法，使其表现更完善。

<!--more-->

## 目录
- [Markdown语法学习][1]
  - [语法补充][2]
  - [Markdown简介][3]  
  - [基本语法][4]
	   - [标题][5]
	   - [分隔线][6]
	   - [强调][7]
	   - [链接][8]
	   - [图片][9]
	   - [列表][10]
	   - [表格][11]
	   - [引用][12]
	   - [代码块][13]
 - [扩展语法][14] 
   - [复选框][15] 
   - [LaTeX 公式][16]
	- [流程图][17]
	- [流程图语法及解释][18]
	- [时序图][19]



---- 
## Markdown简介

> Markdown 是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档，然后转换成格式丰富的HTML页面。    —— [维基百科][20]

你现在读的这些文字，就是使用简单的符号标识不同的标题，将某些文字标记为**粗体**或者*斜体*，创建一个[链接][21].
---- 
## 基本语法
### 标题
\#号数量标示标题大小，
\# 一号标题
\#\# 二号标题
\#\#\# 三号标题
\#\#\#\# 四号标题
\#\#\#\## 五号标题
\#\#\#\### 六号标题\`

展示出来的样式
# 一号标题
## 二号标题
### 三号标题
#### 四号标题
##### 五号标题
###### 六号标题
---- 
### 分隔线
通过利用分隔线可以使内容保持距离，使阅读者更容易阅读。
语法为\*\*\*
**注意**：使用\*\*\*,或---(三个减号)，或\_\_\_(三个下划线)，均能实现此效果。
效果为下面这货
---- 
### 强调

使用\**加粗强调*\*即可实现为包含内容强调的效果
效果为**加粗强调**
使用\*斜体强调\*即可实现为包含内容强调的效果
效果为*斜体强调*
---- 
### 链接
语法[百度] (www.baidu.com)以此实现起链接的效果
效果为[百度][22]
另外链接部分可以改为文章内的标题，实现文内的锚点链接
语法[基本语法] (#基本语法)
效果为[基本语法][23]
---- 


### 图片

语法与链接很像，不过前面要加上一个!
语法
`! [图片名] (图片链接)`
注意有的Markdown不支持本地文件上传，需要图片有网络地址，不过「简书」上支持截图直接上传和拖动直接上传，很是方便。
---- 

### 列表
列表分有序列表和无序列表
有序的很简单啦
`1. 有序1`
`2. 有序2`
效果为

1. 有序1
2. 有序2

而无序的语法为
```
- 无序
* 无序
+无序
```

> **注意**：使用-，\*，+都可以实现无序的排列，且没有先后顺序之分。但无序有一种包含的关系，在Markdown的语法里最高级的无序是实体黑心圆，次一级是空心圆，再次一次是实体正方形。
> 另外有序列表和无序列表中间需要分隔，不然会出现一些排版上的错误，大家可以动手体验一下就明白我说的是什么意思啦。

正常效果展示

- 无序
	* 无序
		+ 无序


---- 

### 表格
表格的语法在基本语法里麻烦一些，不过据粥粥实际使用来说，用个两三回就可以熟练掌握了，这里也会介绍的尽量仔细，方便其他读者查看。
语法：

第一栏`|表头1|表头2|表头3|`
第二栏`|---|---|---|` 

 **注意**：必须有第二栏\竖线的内容列表才能显示出来，如我们添加以下表格信息。  


\| 项目  |  价格 |  数量  |
| :--- | -----:| :---: |
| 电脑  |￥5600 |  5    |
| 手机  |￥4300 |  12   |
\| 冰箱  |￥3100 | 234   |


展示效果如下

| 项目      |    价格 | 数量 |
| :---- | ---:| :-: |
| 电脑      | ￥5600  |  5   |
| 手机      | ￥4300  |  12  |
| iPad     |￥3100   | 234  |


**补充**：大家可能注意到第二栏中的：，这货就是用来做对齐用的，语法如下：
左对齐：:----
右对齐：----:
居中对齐：:----:
大家在实际使用中试一两次很容易就明了啦。

---

### 引用

语法为\>引用内容
嵌套的语法为\>\>引用也可以嵌套
效果为

> 引用内容
> > 引用也可以嵌套呀 

---

### 代码块
下面就是一堆代码
若是一行的话，可以用\`代码内容\`
效果如
`代码内容`

若是太多的话，直接
\`\`\`代码块内容\`\`\`

效果如下

``` python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None
class SomeClass:
    pass
```

---- 

## 扩展语法


### 复选框

使用 `- [ ]` 和 `- [x]` 语法可以创建复选框，实现 todo-list 等功能。效果如：

- [x] 已完成事项
- [ ] 待办事项1
- [ ] 待办事项2

---- 

### LaTeX 公式

可以创建行内公式，例如 $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$。或者块级公式：

效果如
$$	x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$


---- 

### 流程图
流程图和时序属于Markdown中的扩展语法，因此在某些仅支持基本语法编辑器的页面中可能无法显示效果，大家可以换其他的试试，不过太嫌麻烦的话，用其他更专业的流程图工具会更好表现一些，毕竟Md更适用于标记文本信息，如果想查看实际效果，可以**复制**下面代码到[马克飞象][24]的在线编辑器中试一下。
这里主要补充一些粥粥搜集来的知识。

```flow
st=>start: Start|past:>http://www.google.com[]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes 
or No?|approved:>http://www.baidu.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```


### 流程图语法及解释

语法如下

```flow
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes 
or No?|approved:>http://www.baidu.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```

流程图的语法大体分为两面，第一段用来定义元素，第二段用来连接元素
如tag=\>type: content:\>url
- 定义元素
tag是一个标签，在第二段连接元素时用
type是这个标签的类型，常见的类型有
```
- start
- end
- operation
- subroutine
- condition
-inputoutput

condition就是流程图的框里要写的内容，中英文均可，但是type后的冒号和文本间一定要有个空格，
不然会出问题，url指向一个连接，与框框中的文本绑定。
```

- 连接元素
	直接用-\>连接两个元素，condition有yes和no两个分支，因此要写成cond(yes)  cond(no)



---- 

### 时序图:


```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am fine, thanks!
```


效果如下

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am fine, thanks!
```


> **注意：**想了解更多，请查看**流程图**[语法][25]以及**时序图**[语法][26]。


[1]:	#markdown%E8%AF%AD%E6%B3%95%E5%AD%A6%E4%B9%A0
[2]:	#%E8%AF%AD%E6%B3%95%E8%A1%A5%E5%85%85
[3]:	#markdown%E7%AE%80%E4%BB%8B
[4]:	#%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95
[5]:	#%E6%A0%87%E9%A2%98
[6]:	#%E5%88%86%E9%9A%94%E7%BA%BF
[7]:	#%E5%BC%BA%E8%B0%83
[8]:	#%E9%93%BE%E6%8E%A5
[9]:	#%E5%9B%BE%E7%89%87
[10]:	#%E5%88%97%E8%A1%A8
[11]:	#%E8%A1%A8%E6%A0%BC
[12]:	#%E5%BC%95%E7%94%A8
[13]:	#%E4%BB%A3%E7%A0%81%E5%9D%97
[14]:	#%E6%89%A9%E5%B1%95%E8%AF%AD%E6%B3%95
[15]:	#%E5%A4%8D%E9%80%89%E6%A1%86
[16]:	#latex%E5%85%AC%E5%BC%8F
[17]:	#%E6%B5%81%E7%A8%8B%E5%9B%BE
[18]:	#%E6%B5%81%E7%A8%8B%E5%9B%BE%E8%AF%AD%E6%B3%95%E5%8F%8A%E8%A7%A3%E9%87%8A
[19]:	#%E6%97%B6%E5%BA%8F%E5%9B%BE
[20]:	https://zh.wikipedia.org/wiki/Markdown
[21]:	http://www.example.com
[22]:	www.baidu.com
[23]:	#%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95
[24]:	https://maxiang.io/
[25]:	http://adrai.github.io/flowchart.js/
[26]:	http://bramp.github.io/js-sequence-diagrams/