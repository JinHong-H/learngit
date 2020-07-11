# 实例

***

## 1. 基础





+



### 1.4 图像

+ HTML 图像是通过 ```<img>```标签进行定义的。

```(html)
<img src="w3school.jpg" width="104" height="142" />
```

注释：图像的名称和尺寸是以属性的形式提供的



### 1.6 注释

```<!-- This is a comment -->```

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



## 6. 引用

### 6.1 ```<q>``` 用于短的引用

+ ```<q>``` 元素定义短的引用。

+ 浏览器通常会为 ```<q>```元素包围引号。

### 6.2 用于长引用的  ```<blockquote>```

+ HTML ```<blockquote>``` 元素定义被引用的节。

+ 浏览器通常会对 ```<blockquote>``` 元素进行缩进处理。
