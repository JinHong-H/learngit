# HTML5 Input类型

## color

+ color 类型用在input字段主要用于选取颜色

实例：

```(html)
<input type="color" name="favcolor">
```

## date

+ date 类型可以实现从一个日期选择器选择一个日期

实例：

```(html)
 <input type="date" name="bday">
```

## email

+ email 类型用于应该包含 e-mail 地址的输入域。

实例：

```(html)
 <input type="email" name="email">
```

## month

+ month 类型允许你选择一个月份。

```(html)
<input type="month" name="bdaymonth">
```

## number

+ number 类型用于应该包含数值的输入域。

```(html)
<input type="number" name="quantity" min="1" max="5">
```

+ 还能够设定对所接受的数字的限定：

|属性|描述|
|--|--|
|disabled|规定输入字段是禁用的
|max|规定允许的最大值
|maxlength|规定输入字段的最大字符长度
|min|规定允许的最小值
|pattern|规定用于验证输入字段的模式
|readonly|规定输入字段的值无法修改
|required|规定输入字段的值是必需的
|size|规定输入字段中的可见字符数
|step|规定输入字段的合法数字间隔
|value|规定输入字段的默认值

## range

+ range 类型用于应该包含一定范围内数字值的输入域。

+ range 类型显示为滑动条。

```(html)
<input type="range" name="points" min="1" max="10">
```

## search

+ search 类型用于搜索域，比如站点搜索或 Google 搜索。

```(html)
Search Google: <input type="search" name="googlesearch">
```

## tel

+ 定义输入电话号码字段

```(html)
<input type="tel" name="usrtel">
```

## time

+ 用于选择一个时间

```(html)
<input type="time" name="usr_time">
```

## url

+ url 类型用于应该包含 URL 地址的输入域。

+ 在提交表单时，会自动验证 url 域的值。

```(html)
 <input type="url" name="homepage">
```

## week

+ week类型用于选择周和年

```(html)
<input type="week" name="week_year">
```

### 实例

```(html)
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<body>

<form action="demo-form.php">
  选择你喜欢的颜色: <input type="color" name="favcolor"><br>
  <input type="submit">
</form>
<form action="demo-form.php">
  生日: <input type="date" name="bday">
  <input type="submit">
</form>
<form action="demo-form.php">
  E-mail: <input type="email" name="usremail">
  <input type="submit">
</form>

<p><b>注意:</b> Internet Explorer 9  及更早 IE 版本不支持 type="email" 。</p>

<form action="demo-form.php">
  生日 ( 月和年 ): <input type="month" name="bdaymonth">
  <input type="submit">
</form>

<form action="demo-form.php">
  数量 ( 1 到 5 之间): <input type="number" name="quantity" min="1" max="5">
  <input type="submit">
</form>

<p><b>注意:</b>Internet Explorer 9 及更早 IE 版本不支持 type="number" 。</p>

<form action="demo-form.php" method="get">
Points: <input type="range" name="points" min="1" max="10">
<input type="submit">
</form>

<form action="demo-form.php">
  Search Google: <input type="search" name="googlesearch"><br>
  <input type="submit">
</form>

<p><b>注意:</b> Internet Explorer 9 及更早 IE 版本不支持 type="range"。</p>

<form action="demo-form.php">
  电话号码: <input type="tel" name="usrtel"><br>
  <input type="submit">
</form>

<form action="demo-form.php">
  添加你的主页: <input type="url" name="homepage"><br>
  <input type="submit">
</form>

<form action="demo-form.php">
  选择周: <input type="week" name="year_week">
  <input type="submit">
</form>


</body>
</html>
```
