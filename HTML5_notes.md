### HTML基本（常用）标签的整理:

[HTML 标准属性参考手册]([超链接地址](https://www.w3school.com.cn/tags/html_ref_standardattributes.asp) "超链接title")

#### 基本

```(HTML)
<html>…</html> 定义 HTML 文档

<head>…</head> 文档的信息

<meta> HTML 文档的元信息

<title>…</title> 文档的标题

<link> 文档与外部资源的关系

<style>…</style> 文档的样式信息

<body>…</body> 可见的页面内容

<!--…--> 注释
```

#### 文本

```(HTML)
<h1>...</h1> 标题字大小（h1~h6）

<b>...</b> 粗体字

<strong>...</strong> 粗体字(强调)

<i>...</i> 斜体字

<em>...</em> 斜体字(强调)

<u>...</u> 下划线

<del>...</del> 删除线(表示删除)

<center>…</center> 居中文本(HTML5已不支持center标签，可用样式text-align:center代替)

<ul>…</ul> 无序列表

<ol>…</ol> 有序列表

<li>…</li> 列表项目

<a href="...">…</a> 超链接

<font> 定义文本字体尺寸、颜色、大小

<sub> 下标

<sup> 上标

<br> 换行

<p> 段落
```

#### 图形

```(HTML)
<img src=' "..."> 定义图像
<hr> 水平线
```

### 表格

```(HTML)
<table>…</table> 定义表格

<th>…</th> 定义表格中的表头单元格

<tr>…</tr> 定义表格中的行

<td>…</td> 定义表格中的单元
```

#### 其它

```(HTML)
<form>…</form> 定义供用户输入的 HTML 表单

<frame> 定义框架集的窗口或框架
```

# 实例

***

## 1. 基础

### 1.1 标题

+ HTML 标题（Heading）是通过``` <h1> - <h6> ```等标签进行定义的。

```(html)
<h1>This is a heading</h1>
<h2>This is a heading</h2>
<h3>This is a heading</h3>
```

+ 浏览器会自动地在标题的前后添加空行。

+ 默认情况下，HTML 会自动地在块级元素前后添加一个额外的空行，比如段落、标题元素前后。

### 1.2 段落

+ HTML 段落是通过 ```<p>``` 标签进行定义的。
  
```(HTML)
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

+

### 1.3 链接

+ HTML 链接是通过```<a>```标签进行定义的。

```(html)
<a href="http://www.w3school.com.cn">This is a link(链接名)</a>
```

### 1.4 图像

+ HTML 图像是通过 ```<img>```标签进行定义的。

```(html)
<img src="w3school.jpg" width="104" height="142" />
```

注释：图像的名称和尺寸是以属性的形式提供的

### 1.5 水平线

+ ```<hr />``` 标签在 HTML 页面中创建水平线。

+ hr 元素可用于分隔内容。

```(html)
<p>This is a paragraph</p>
<hr />
<p>This is a paragraph</p>
<hr />
<p>This is a paragraph</p>
```

### 1.6 注释

```<!-- This is a comment -->```

***

## 2. HTML元素

+ HTML 文档是由 HTML 元素定义的。

+ **HTML 元素指的是从开始标签（start tag）到结束标签（end tag）的所有代码**

+ 开始标签常被称为开放标签（opening tag），结束标签常称为闭合标签（closing tag）

### 2.1 元素语法

+ HTML 元素以开始标签起始
+ HTML 元素以结束标签终止
+ ***元素的内容是开始标签与结束标签之间的内容***
+ 某些 HTML 元素具有空内容（empty content）
+ 空元素在开始标签中进行关闭（以开始标签的结束而结束）
+ 大多数 HTML 元素可拥有属性

### 2.2 空的 HTML 元素

+ 没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的。

+ ```<br>``` 就是没有关闭标签的空元素（```<br>``` 标签定义换行）。

+ 在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭。

+ 在开始标签中添加斜杠，比如```<br />(推荐使用)```，是关闭空元素的正确方法，HTML、XHTML 和 XML 都接受这种方式。

***

## 3. HTML属性

### 3.1 HTML 属性

+ HTML 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。

+ 属性总是以名称/值对的形式出现，比如：name="value"。

+ 属性总是在 HTML 元素的开始标签中规定

### 3.2 属性实例

#### 3.2.1 HTML 链接由 ```<a>``` 标签定义。链接的地址在 href 属性中指定

```(html)
<a href="http://www.w3school.com.cn">This is a link</a>
```

#### 3.2.2 居中排列标题

+ ```<h1>``` 定义标题的开始。

+ ```<h1 align="center">``` 拥有关于对齐方式的附加信息

```(html)
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">

<html>

<body>

<h1 align="center">This is heading 1</h1>

<p>上面的标题在页面中进行了居中排列。上面的标题在页面中进行了居中排列。上面的标题在页面中进行了居中排列。</p>

</body>
</html>

```

#### 3.2.3 背景颜色

+ ```<body>``` 定义 HTML 文档的主体。

+ ```<body bgcolor="yellow">``` 拥有关于背景颜色的附加信息
  
#### 3.2.4 始终为属性值加引号

+ 属性值应该始终被包括在引号内。双引号是最常用的，不过使用单引号也没有问题。

***

## 4. 样式

### 4.1 背景颜色

+ background-color 属性为元素定义了背景颜色

```(html)
<html>

<body style="background-color:yellow">
<h2 style="background-color:red">This is a heading</h2>
<p style="background-color:green">This is a paragraph.</p>
</body>

</html>
```

### 4.2 字体、颜色和尺寸

+ font-family、color 以及 font-size 属性分别定义元素中文本的字体系列、颜色和字体尺寸：

```(html)
<html>

<body>
<h1 style="text-align:center">This is a heading</h1>
<p>The heading above is aligned to the center of this page.</p>
</body>

</html>
```

***

## 5. 格式化

|标签|描述|
|  ----  | ----  |
| ```<b>```  | 定义粗体文字 |
| ```<big>```  | 定义大号文字 |
| ```<em>```  | 定义着重文字 |
| ```<i>```  | 定义斜体字 |
| ```<small>```  | 定义小号文字 |
| ```<strong>```  | 加重语气 |
| ```<sub>```  | 定义下标字 |
| ```<sup>```  | 定义上标字 |
| ```<in>```  | 定义插入字 |
| ```<del>```  | 定义删除字 |

### 5.1 文本格式化

```(html)
<html>

<body>

<b>This text is bold</b>

<br />

<strong>This text is strong</strong>

<br />

<big>This text is big</big>

<br />

<em>This text is emphasized</em>

<br />

<i>This text is italic</i>

<br />

<small>This text is small</small>

<br />

This text contains
<sub>subscript</sub>

<br />

This text contains
<sup>superscript</sup>

</body>
</html>

```

### 5.2 预格式文本

```(html)
<html>

<body>

<pre>
这是
预格式文本。
它保留了      空格
和换行。
</pre>

<p>pre 标签很适合显示计算机代码：</p>

<pre>
for i = 1 to 10
     print i
next i
</pre>

</body>
</html>
```

### 5.3 地址

```(html)
<!DOCTYPE html>
<html>
<body>

<address>
Written by <a href="mailto:webmaster@example.com">Donald Duck</a>.<br>
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>

</body>
</html>
```

### 5.4 缩写和首字母缩写

```(html)
<html>

<body>

<abbr title="etcetera">etc.</abbr>
<br />
<acronym title="World Wide Web">WWW</acronym>

<p>在某些浏览器中，当您把鼠标移至缩略词语上时，title 可用于展示表达的完整版本。</p>

<p>仅对于 IE 5 中的 acronym 元素有效。</p>

<p>对于 Netscape 6.2 中的 abbr 和 acronym 元素都有效。</p>

</body>
</html>
```

## 6. 引用

### 6.1 ```<q>``` 用于短的引用

+ ```<q>``` 元素定义短的引用。

+ 浏览器通常会为 ```<q>```元素包围引号。

### 6.2 用于长引用的  ```<blockquote>```

+ HTML ```<blockquote>``` 元素定义被引用的节。

+ 浏览器通常会对 ```<blockquote>``` 元素进行缩进处理。

```(html)
<p>以下内容引用自 WWF 的网站：</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
五十年来，WWF 一直致力于保护自然界的未来。
世界领先的环保组织，WWF 工作于 100 个国家，
并得到美国一百二十万会员及全球近五百万会员的支持。
</blockquote>
```
