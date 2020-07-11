# 表格

### 表格常用标签

|标签|描述|
|--|--|
|\<table>|定义表格|
|\<th>|定义表头|
|\<tr>|定义行|
|\<td>|定义表格单元|
|\<caption>|定义表格标题|
|\<colgroup>|定义表格列的组|
|\<col>|定义表格列的属性|
|\<thead>|定义表格页眉|
|\<tbody>|定义表格主体|
|\<tfool>|定义表格的页脚|

### 表格

+ 表格由 \<table> 标签来定义。每个表格均有若干行（由 \<tr> 标签定义），每行被分割为若干单元格（由 \<td> 标签定义）。
+ 字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

### 表格和边框属性

+ \<table border = "x"> (x = 1,有边框，x = 0时，无边框)如果不定义边框属性(border)，表格将不显示边框。

### 表格表头

+ 表格的表头使用 \<th> 标签进行定义。

+ 大多数浏览器会把表头显示为粗体居中的文本

实例：

```(html)
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<body>

<h4>这个表格有边框:</h4>
<table border = "1">
<tr>
  <td>100</td>
  <td>200</td>
  <td>300</td>
</tr>
<tr>
  <td>400</td>
  <td>500</td>
  <td>600</td>
</tr>
</table>

<h4>这个表格没有边框:</h4>
<table>
<tr>
  <td>100</td>
  <td>200</td>
  <td>300</td>
</tr>
<tr>
  <td>400</td>
  <td>500</td>
  <td>600</td>
</tr>
</table>

<h4>这个表格没有边框:</h4>
<table border="0">
<tr>
  <td>100</td>
  <td>200</td>
  <td>300</td>
</tr>
<tr>
  <td>400</td>
  <td>500</td>
  <td>600</td>
</tr>
</table>

</body>
</html>
```