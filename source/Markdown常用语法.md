# Markdown常用语法详解

------

[TOC]

# Markdown 标题语法

------

在标题前面添加井号 #。# 的数量代表了标题的级别。
注意："#" 和 "标题" 之间为保证兼容性要留空格。

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

可选语法：只能达到二级标题
一级标题
=======
二级标题
-------
```

# Markdown 换行语法

------

在一行的末尾添加两个或多个空格，然后按回车键,即可创建一个换行`<br>`。
也可直接添加`<br>`。部分编辑器会自动添加换行符，如：Typora。

# Markdown 强调语法

------

示例：

```
*斜体*
**粗体**
***加粗斜体***
~~删除线~~
===高亮==
上标m^2^
下标H~2~O
```

效果：
*斜体*
**粗体**
***加粗斜体***
~~删除线~~
===高亮==
上标m^2^
下标H~2~O

# Markdown 引用语法

------

示例：

```
>一级引用
>>二级引用
>>>三级引用
```

效果：

> 一级引用
> > 二级引用
> >
> > > 三级引用

# Markdown 列表语法

------

## 无序列表

使用 *、+、- 表示无序列表，缩进一个或多个列表项可创建嵌套列表。
主意：一个级别只使用一种符号。

示例：

```
* 列表1
	+ 列表2
		* 列表3
		* 列表3
	+ 列表2
* 列表1
* 列表1
```

效果：

* 列表1
	+ 列表2
		* 列表3
		* 列表3
	+ 列表2
* 列表1
* 列表1

## 有序列表

添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始。
注意：
	* 英文句点后面一定要有一个空格。
	* 无论序号如何填写，预览时同一级别都会重新自动编号。

示例：
```
1. 列表1
	1. 列表2
		1. 列表3
		1. 列表3
	1. 列表2
1. 列表1
```

效果：

1. 列表1
	1. 列表2
		1. 列表3
		1. 列表3
	1. 列表2
1. 列表1

## 待办列表

使用"-"和"[ ]"表示待办列表。
注意："-"后面一定要有一个空格，"[ ]"中括号内一定要有空格。

示例：
```
- [ ] 未完成
- [x] 已完成
```
效果：
- [ ] 未完成
- [x] 已完成

# Markdown 代码语法

------

## 单行代码

要将单词或短语表示为代码，请将其包裹在反引号 ( ` ) 中。

这个一个\``单行代码`\`示例。

```
Use `code` in your Markdown file.
```

## 多行代码

要将多行表示为代码块，请在其前后加三个反引号(`````）或三个波浪号（~~~）。

示例：
```java
public static main(String[] args){
	public class HelloWorld(){				  
		system.out.println("Helloworld!");
	}
}
```

# Markdown 分隔线语法

------

单独一行上使用三个或多个星号 (***)、破折号 (---) 或下划线 (___) ，并且不能包含其他内容。为了兼容性，请在分隔线的前后均添加空白行。

# Markdown 链接语法

------

## 行内式超链接

* 行内超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")`
* "超链接title"是鼠标悬停在链接上时会出现的文字，这个title是可选的。跟链接地址之间以空格分隔。
* 这是不带title[哔哩哔哩](www.bilibili.com)
* 这里是带title[哔哩哔哩](www.bilibili.com "哔哩哔哩")

## 引用式超链接

* 引用超链接Markdown语法代码第一部分：`[超链接显示名][超链接标签]`
* 引用超链接Markdown语法代码第二部分：`[超链接标签]: 超链接地址 "超链接title"`
* "超链接title"是可选的。
* 引用式超链接一般用在同一链接多次出现，且链接地址可变的情况，方便更改链接地址。
* 注意空格分隔，代码第二部分，不会显示出来。

示例：

```
在内容搜索上，我喜欢用[百度][2]、[谷歌][1]、[今日头条][今日头条]等，
随着[今日头条][今日头条]的崛起，已经逐渐使用[头条][今日头条]来搜索需要的内容。

[1]: https://www.google.com
[2]: https://www.baidu.com "baidu搜索引擎"
[今日头条]: <https://www.toutiao.com> "头条更懂你"
```

效果：

在内容搜索上，我喜欢用[百度][2]、[谷歌][1]、[今日头条][今日头条]等，
随着[今日头条][今日头条]的崛起，已经逐渐使用[头条][今日头条]来搜索需要的内容。

[1]: https://www.google.com
[2]: https://www.baidu.com "baidu搜索引擎"
[今日头条]: <https://www.toutiao.com> "头条更懂你"

## 网址和Email地址

使用尖括号可以很方便地把URL或者email地址变成可点击的链接。

示例：

```
<https://markdown.com.cn>
<fake@example.com>
```

效果：

<https://markdown.com.cn>
<fake@example.com>

## 链接最佳方式
不同的 Markdown 应用程序处理URL中间的空格方式不一样。为了兼容性，请尽量使用`%20`代替空格。

正确处理：
`[link](https://www.example.com/my%20great%20page)`

错误处理：
`[link](https://www.example.com/my great page)`

# Markdown 图片语法

------

* 插入图片语法代码：`![图片alt](图片链接 "图片title")`
* 链接图片语法代码: `[插入图片语法代码](超链接地址)`

调整图片位置、大小
![描述](https://img-blog.csdnimg.cn/20191209162719837.png)
居中：
![描述](https://img-blog.csdnimg.cn/20191209162719837.png#pic_center)
居中 + 调整大小：
注意"="符号前面的空格
![描述](https://img-blog.csdnimg.cn/20191209162719837.png#pic_center =400x400)

仅调整大小：
![描述](https://img-blog.csdnimg.cn/20191209162719837.png =200x200)


示例：网络图片
```
![头像图片](https://sf3-ttcdn-tos.pstatp.com/img/labis/d41f97e477d54ffa5060cd1abd9857bb~tplv-tt-cs0:360:360.webp "这是头像")
```
效果：

![头像图片](https://sf3-ttcdn-tos.pstatp.com/img/labis/d41f97e477d54ffa5060cd1abd9857bb~tplv-tt-cs0:360:360.webp "这是头像")

示例：本地图片
```
![头像图片](./Markdown常用语法images/0cd63.jpg "这是头像图片")
```

效果：
![头像图片](./Markdown常用语法images/0cd63.jpg "这是头像图片")
[![头像图片](./Markdown常用语法images/0cd63.jpg "这是头像图片")](www.baidu.com)

# Markdown 表格（拓展语法）

* 要添加表，请使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列。您可以选择在表的任一端添加管道。

* 左侧，右侧或两侧添加冒号（:），将列中的文本对齐到左侧，右侧或中心。

* 可以在表格中设置文本格式。例如，您可以添加链接，代码（仅反引号（```）中的单词或短语，而不是代码块）和强调。

    您不能添加标题，块引用，列表，水平规则，图像或HTML标签。

示例：
```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```
效果：
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

# Markdown 脚注（拓展语法）

* 脚注第一部分：`[^1]`
* 脚注第二部分：`[^1]: 这里是脚注内容！`

示例：
```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: Here's one with multiple paragraphs and code.
```
效果：
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: Here's one with multiple paragraphs and code.

# Markdown 定义列表

目前部分编辑器不支持

示例：
```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```
效果：

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.






参考：
1. <https://markdown.com.cn/basic-syntax/>
1. <https://markdown.com.cn/extended-syntax/>
1. <https://blog.csdn.net/witnessai1/article/details/52551362>
1. <https://blog.csdn.net/u014061630/article/details/81359144>
1. <https://blog.csdn.net/afei__/article/details/80717153>

