# HTML

```html
<!DOCTYPE html>				#声明为HTML5文档
<html>						#根元素
    <head>					#包含meta数据描述网页
       <meta charset = >	#编码格式
        <title>#文档的标题</title>
        
    </head>
    <body>					#可见的页面内容
      
        <h1>#定义一个大标题</h1>    
        <p>#定义一个段落</p>    
         
	</body>
    
</html>
```

超文本标记语言，用标记标签来描述网页

标签:<关键词>，通常成对出现



浏览器读取HTML文件并显示

| 属性名      | 元素                          | 说明                                  |
| ----------- | ----------------------------- | ------------------------------------- |
| id          | all                           | 指定<u>唯一</u>标识符                 |
| class       | all                           | 元素指定类名，用于class或js           |
| style       | all                           | 直接应用css样式                       |
| title       | all                           | 悬停显示额外的提示信息                |
| data-*      | all                           | 存储自定义数据                        |
| href        | <a>,<link>                    | 指定链接的目标URL                     |
| src         | <img>,<script>,<iframe>       | 指定外部资源（图片、脚本、框架）的URL |
| alt         | <img>                         | 提供图片无法显示时的代替文本          |
| type        | <input>,<button>              | 指定输入控件的类型                    |
| value       | <input>,<button>,<option>     | 元素初始值                            |
| disabled    | all                           | 禁用元素（无需值）                    |
| checked     | <input type="checkbox/radio"> | 指定复选框或单选按钮是否被选中        |
| placeholder | <input>,<textarea>            | 输入框内显示提示文本                  |
| target      | <form>,<a>                    | 指定连接或表单提交的目标窗口或框架    |
| readonly    | <input>                       | 输入框只读（无需值）                  |
| required    |                               | 输入字段为必填项（无需值）            |
| autoplay    | <audio>,<video>               | 自动播放媒体                          |
| onclick     |                               | 点击元素触发                          |
| onmouseover |                               | 悬停触发                              |
| onchange    |                               | 值发生变化时触发                      |



注释：

<!-- 这是一个注释 -->

### 样式：

- 使用 attribute 设置 HTML 元素的样式`style=“property：value;”`
- 用于背景色`background-color`
- 用于文本颜色`color`
- 用于文本字体`font-family`
- 用于文本大小`font-size`
- 用于文本对齐`text-align`



- `<b>`- 粗体文本

- `<strong>`- 重要文本

- `<i>`- 斜体文本

- `<em>`- 强调的文本

- `<mark>`- 标记的文本

- `<small>`- 较小的文本

- `<del>`- 删除的文本

- `<ins>`- 插入的文本

- `<sub>`- 下标文本

- `<sup>`- 上标文本

  

### 头部:

	<title>:文档的标题
	<base href = "">:全文档链接标签的初始地址
	<link>:链接到外部资源
	<meta>:元数据
	*name属性和http-equiv属性
	<style>:样式文件



### css：渲染html标签的样式

  三种添加方式：

​		1.内联-html元素内使用；<style = "property: value">

​		2.内部样式表-<head>标签内（仅对于当前页面有效）<style type= "text/css">

​		3.外部样式表-独立文件，样式文件会被暂时缓存(修改时需CTRL+F5)（链接 or 导入）

```html
<link type= "text/css" rel = "stylesheet" href = "url"/>
<!-- type:MIME类型 rel:设置目标文件与当前文档的关系 -->

<!-- 以下为外部样式表文件 -->
@charset "utf-8";
p{

	width : 400px;
	color : ;
	font-size : ;
	font-famliy : ;
	background-color : ;
	text-align : ;
}
```

​		优先级：内嵌>内部>外部



### 图像：

```html
<img>:插入图片	
<map>:定义图像地图 需在<img>中插入属性 usemap="#" <map name = "">
<area>:定义地图中可点击区域
```



### 表格<table>标签

​		<tr>:table row

​		<td>:table data

​		<th>:table header

​		<caption>:整个表格标题

​		属性：colspan、rowspan（跨行）cellpadding（格边距）cellspacing（格间距）



### 列表：

	<ul>:无序列表
	    <li><li/>
	    <ul style="list-style-type:disc/circle/square">
	<ol>:有序列表
		属性:type不同了类型排列
	<dl>:自定义列表
		<dt>:自定义列表项
		<dd>:自定义列表描述



### 区块：(组合元素)

	<div>:块级元素（占用整行），独占一行，可设置样式，页面大块结构
	<span>:内联元素（只占内容宽度），适合对文本和行内元素样式化



### 布局:

​		<div>:待补充

​		<table>:待补充



### 表单（用户交互）：

​		**<form>**属性:

​			**action**：表单提交的目标urls

​			**method**：提交时使用的HTTP方法（<u>post表单数据会包含在表单体内然后发送给服务器,用于提交敏感数据、get表单数据会附在action属性的url上，以?为分隔符</u>）



​		**<label>**标签为input元素定义标注，利用for属性可和有相同id的元素绑定



​		**<input>**属性：

​			**type**："text"(文本) / "password"(密码) / "radio"(单选按钮) / "submit"(提交) / "checkbox"(复选框)/

​			**id**：关联<label>

​			**name**：标识表单字段，传入表单时作为键（key）



​		**<select>**（下拉列表）属性：														

​			**name**：键

​		**<option value = "">**：可选项；

​			**selected**：默认选择

​		

​		**<textarea>**（文本域）属性：

​			rows：

​			cols：



### 框架：

​		同一窗口浏览多页面

​	**<iframe src = "urls"></iframe>**属性：

​			height

​			width

​			frameborder
