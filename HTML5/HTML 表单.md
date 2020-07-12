# 表单和输入

### 常用标签

|标签|描述|
|--|--|
|\<form>|定义供用户输入的表单|
|\<input>|定义输入域|
|\<textarea>|定义文本域 (一个多行的输入控件)|
|\<label>|定义了\<input>元素的标签，一般为输入标题|
|\<fieldset>|定义了一组相关的表单元素，并使用外框包含起来|
|\<legend>|定义了 \<fieldset> 元素的标题|
|\<select>|定义了下拉选项列表|
|\<optgroup>|定义选项组|
|\<option>|定义下拉列表中的选项|
|\<button>|定义一个点击按钮|
|\<datalist>(new)|指定一个预先定义|的输入控件选项列表
|\<keygen>(new)|定义了表单的密钥对|生|成器字段
|\<output>(new)|定义一个计算结果|

#### 表单

+ 表单是一个包含表单元素的区域。

+ 表单元素是允许用户在表单中输入内容,比如：文本域(textarea)、下拉列表、单选框(radio-buttons)、复选框(checkboxes)等等。

表单使用表单标签 \<form> 来设置:

```(html)
<form>
.
input 元素
.
</form>
```

#### 输入元素

+ 多数情况下被用到的表单标签是输入标签（\<input>）。

+ 输入类型是由类型属性（type）定义的。大多数经常被用到的输入类型如下：

##### 文本域

+ 文本域通过\<input type="text"> 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。

```(html)
<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>
```

##### 密码字段

+ 密码字段通过标签 ```<input type="password"> ```来定义:

```(html)
<form>
Password: <input type="password" name="pwd">
</form>
```

##### 单选按钮

+ ````<input type="radio">```` 标签定义了表单单选框选项

```
<form>
<input type="radio" name="sex" value="male">Male<br>
<input type="radio" name="sex" value="female">Female
</form>
```

##### 复选框

+ ```<input type="checkbox">``` 定义了复选框. 用户需要从若干给定的选择中选取一个或若干选项。

```(html)
<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car
</form>
```

##### 提交按钮

+ ```<input type="submit">```定义了提交按钮.

+ 当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理。

```(html)
<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>
```
