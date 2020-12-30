---
title: Web前端学习笔记（实训）
date: 2020-12-17 10:20:06
tags:
 - Web前端
 - 实训
 - 学习笔记
 - html
 - css
 - JavaScript
categories:
 - 实训
---

## HTML

html是超文本标记语言，专用于开发和用户交互的界面，也就是浏览器打开的都是页面

IDE：开发工具，web前端技术的IDE  ：hbuilder、sublime、idea

html是一个标记语言：

### HTML标记

> ①、所有的标记都必须有开始和结束，开始标记   结束标记
>
> ②、所有的标记都必须放在<>括起来
>
> ③、有一种比较特殊的标记  空标记，没有值的标记叫空标记
>
> ④、标记的值，开始标记和结束标记中间的内容都叫做标记的值
>
> ⑤、标记可以合理嵌套，外层叫父标记  内层子标记
>
> ⑥、在开始标记中可以加多个属性，属性由两部分组成，属性名=属性值，属性值必须用‘’或者“”括起来，多个属性用空格分隔。

### Helloword

> ①、根标记，html中有一个标记非常特殊，所有的标记都必须放在这个标记内  《html》
>
> ②、两大块，head  body两大块
>
> head：用于设置页面的相关属性，比如标题是？字符编码？....
>
> body：页面的主题部分，也是我们经常写的部分!

### 具体常见的标记

> ①、标题标记，h1---h6

~~~html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		
		<fieldset>
			<legend>登录窗口</legend>
			<!--form:表单标记
				action：用于指明当前表单提交给谁？
				method：当前表单的提交方式  get  post
			-->
			<form action="T1" method="get">
				<div>
					<!--
						type：指明当前输入框的类型：
						=text：说明一个文本输入框
						=passowrd：说明是一个密码输入框
						=radio:单选按钮
						name：用于设置当前输入框的名称---将来是参数的名称
					-->
					登录ID：<input type="text" name="userid" />
				</div>
				<div>
					登录密码：<input type="password" name="password" />
				</div>
				<input value="【登录】" type="submit"/>
			</form>
				
		</fieldset>
		
		
		<fieldset>
			<legend>注册窗口</legend>
			<!--form:表单标记-->
			<form action="T2">
				<div>
					账号ID：<input type="text" name="userid" />
				</div>
				<div>
					账号密码：<input type="password" name="password" />
				</div>
				<div>
					确认密码：<input type="password" name="cmfpwd" />
				</div>
				<div>
					电话号码：<input type="text" name="mobile" />
				</div>
				
				<div>
					<!--
						当单击提交按钮是，会将选中的单选框中的value属性值提交到服务器端
						checked:设置是否选中
					-->
					性别：  男<input type="radio" name="sex" value="nan" checked="checked">
						   女<input type="radio" name="sex" value="nv"/>
					
				</div>
				<div>
					个人喜好：
					体育<input type="checkbox" name="hobby" value="a1"  checked="checked"/>
					看书<input type="checkbox" name="hobby" value="a2"/>
					写代码<input type="checkbox" name="hobby" value="a3"/>
				</div>
				<div>
					你的学历：
					<select name="degree">  <!--下拉列表框-->
						<option>博士</option>  <!--下拉选项-->
						<option>硕士</option>
						<option>学士</option>
						<option>其他</option>
					</select>
					
				</div>
				<div>
					个人描述:
					<textarea name="desc" rows="10" cols="70"></textarea>  <!--文本区-->
					
				</div>
				<!--
					submit:用于提交当前表单
					reset：重置当前表单
				-->
				<input value="【注册】" type="submit"/>
				<input value="【重置】" type="reset"/>
			</form>
				
		</fieldset>
	</body>
</html>



<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<!--div默认是换行的，而span是不换行-->
		<div>我是div的值1</div>
		<div>我是div的值2</div>
		<div>我是div的值3</div>
		
		<span>我是span的值1</span>
		<span>我是span的值2</span>
		<span>我是span的值3</span>
	</body>
</html>


<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<!--
			img标记用于设置图片
			src：用于指定图片的URL
			alt：在图片无法显示时，会将alt属性中的值显示到页面上
			title：在鼠标进入到图片上方时，显示的提示内容
			width：设置图片的宽度
			height:设置图片的高度
		-->
		<img src="img/a1.jpg" alt="看看我" title="我是你的忠实粉丝" width="300px" height="300px"/>
		<img src="img/a2.jpg" width="300px" height="300px"/>
		
		<!--如下代码可以完成单击图片后显示目标页面-->
		<a href="index.html">
			<img src="img/a3.jpg" width="300px" height="300px"/>
		</a>
		
	</body>
</html>




<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<!--超链接标记，用于从a页面跳转到b页面
			
			href：指定目标页面的URL
			target:设置目标页面显示的地方  _blank开启一个空的浏览器窗口显示目标页面
		-->
		<a href='index.html' target="_blank">单击我显示index.html页面</a>
		友情链接：
		<a href="http://www.csdn.net">csdn官网</a>
		
		<!--如下用#指定锚名称 即  显示目标页面的同时定位到指定锚位置-->
		<a href="b.html#one">第一章</a>
		<a href="b.html#two">第二章</a>
		<a href="b.html#three">第三章</a>
		
	</body>
</html>


<!--代表当前html的版本是html5版本-->
<!DOCTYPE html>
<!--根标记     标记也叫元素-->
<html>
	<head>
		<!--当前编码方式utf-8  支持汉字   -->
		<meta charset="utf-8" />
		<!--标题-->
		<title>我的第一个网页</title>
	</head>
	<body>
		<!--段落标记-->
		<p>我是第一段</p>
		<p>我是第二段</p>
		<!--换行标记  是一个空标记-->
		<br />
		
		
		
		
		<b>我是<del>加粗</del>显示的内容</b>
		<i>我是斜体字</i>
		
		默认的内容
		<h1>1号标题</h1>
		<h2>2号标题</h2>
		<h3>3号标题</h3>
		
		
	</body>
</html>


<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		
		
		第一章的内容  
		<!--
			通过name属性定义锚名称
			我们可以把锚名称当成一个书签，或者是一个页面
			注意：定义锚除了name属性外，还可以用id属性来定义
		-->
		<a id="one"></a>
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		第二章的内容
		<a id="two"></a>
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		第三章的内容
		<a id="three"></a>
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
		<br />
	</body>
</html>

<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		
		<!--border：设置表格边框的宽度-->
		<table border="1px">
			<!--tr：行-->
			<tr>
				<!--td：列-->
				<td>姓名</td>
				<td>电话</td>
				<td>邮箱</td>
				<td>地址</td>
			</tr>
			<tr>
				<td>刘备</td>
				<td>1333</td>
				<td>liubei@163.com</td>
				<!--rowspan:设置当前单元格跨行-->
				<td rowspan="2">三国</td>
			</tr>
			<tr>
				<!--colspan:设置单元格跨列-->
				<td>关羽</td>
				<td colspan="2">1444</td>
				<!--<td>guanyu@163.com</td>-->
				<!--<td>三国</td>-->
			</tr>
			
		</table>
	</body>
</html>





<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		
		<button onclick="alert('abc');">单机我</button>
	</body>
</html>

~~~

## CSS

### 前置知识：

①、css叫层叠样式表。专门用于设置html页面的样式

②、css代码写在哪？

Ⅰ 、可以写在<style>元素中

Ⅱ、可以写在独立的以css为扩展名的文件中

Ⅲ、可以写在html元素的style属性中

### css的语法

selector{

样是名称：样式值;

样是名称：样式值;

.....

}

### css选择器

匹配被操作的元素。css选择器在jquery技术中照样适用

> ~~~css
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		
> 		<style type="text/css">
> 			/*①:通配符选择器*/
> 			*{
> 				background-color: #00FFFF;
> 			}
> 			/*
> 			 * ②:元素选择器：根据元素的名称匹配元素 ,匹配了所有的对应的html元素
> 			 */
> 			div{
> 				background-color: #FF00FF;
> 			}
> 			/*③:类选择器:根据元素的class属性值匹配元素,注意class属性值是可以重复的，所以一般来讲类选择器都会匹配出来多个元素*/
> 			.c1{
> 				background-color: #0000FF;
> 			}
> 			/*④:id选择器:基于元素的id属性值匹配元素，注意一般来讲，id属性值时不允许重复的，所以一般来讲，id选择器匹配了一个元素*/
> 			#one{
> 				background-color: #44FF55;
> 			}
> 			/*⑤:属性选择器: 匹配了具有href属性的所有html元素*/
> 			[href]{
> 				background-color: #AA9900;
> 			}	
> 			[href="03-img.html"]{
> 				background-color: #FF00FF;
> 			}				
> 		</style>
> 	</head>
> 	<body>
> 		<a href="02-a.html">020202</a>
> 		<a href="03-img.html">030303</a>
> 		
> 		
> 		<div id="one">div11111111</div>
> 		<div id="two">div11111111</div>
> 		
> 		
> 		<hr />
> 		<div>div元素的值1111</div>
> 		<span class="c1">span元素的值11111</span>
> 		<div>div元素的值2222</div>
> 		<span class="c1">span元素的值22222</span>
> 	</body>
> </html>
> 
> 
> 
> 
> 
> 
> 
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style type="text/css">
> 			
> 			/*⑥:后代选择器,如下仅仅匹配了li内部的strong元素，没有在li内部的strong元素匹配不出来*/
> 			li strong{
> 				background-color: #FF00FF;
> 			}
> 			/*⑦:选择器分组，让多个元素的样式相同，用，号分割开来*/
> 			p,div,#id1{
> 				background-color:#0000FF;
> 			}
> 			/*⑧:子元素选择器:只能匹配某个元素的直接子元素*/
> 			li>strong{
> 				enable-background: red;
> 			}
> 			/*⑨:兄弟选择器:兄弟是li的元素*/
> 			li + li {
> 				font-weight:bold;
> 				background-color: #AA9900;
> 			}
> 			/*⑩、伪类选择器  未被访问过的链接的样式*/
> 			a:link{
> 				color: #AA9900;
> 				text-decoration: none;
> 			}
> 			/*鼠标移动到连接上方时*/
> 			a:hover{
> 				text-decoration:underline
> 			}
> 			/*匹配并列的li元素的第一项*/
> 			li:first-child{
> 				background-color: #FF00FF;
> 			}
> 			li:last-child{
> 				color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<a href="08-css.html">080808</a>
> 		
> 		<hr/>
> 		
> 		  <ul>
> 		    <li>List item 1</li>
> 		    <li>List item 2</li>
> 		    <li>List item 3</li>
> 		  </ul>
> 		  <ol>
> 		    <li>List item 1</li>
> 		    <li>List item 2</li>
> 		    <li>List item 3</li>
> 		  </ol>
> 
> 		
> 		<hr />
> 		<hr />
> 		<hr />
> 		<p>我是p元素的值，也是<strong>第一段</strong>内容</p>
> 		<ol>
> 			<li>第一章<span><strong>第一段</strong></span>内容</li>
> 			<li>第一章<span id="id1">第二段</span>内容</li>
> 			<li>第一章<strong>第三段</strong>内容</li>
> 		</ol>
> 		<div>div的值</div>
> 	</body>
> </html>
> 
> ~~~
>
> ~~~ html
> <!--<!DOCTYPE html>-->
> <html>
> 
> 	<head>
> 		<style type="text/css">
> 			/*id选择器   table*/
> 			#customers {
> 				/*设置字体*/
> 				font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
> 				/*表格的宽度，，，，100%--->将表格扩充到整个页面*/
> 				width: 100%;
> 				/*让表格中的边框合并为一个*/	
> 				border-collapse: collapse;
> 			}
> 			
> 			/*选择器分组   后代选择器*/
> 			#customers td,#customers th {
> 				/*设置字体大小*/
> 				font-size: 1em;
> 				/*表格边框为1px宽度,单实线,颜色*/
> 				border: 1px solid #98bf21;
> 				/*设置内边距*/
> 				padding: 3px 7px 2px 7px;
> 			}
> 			
> 			#customers th {
> 				font-size: 1.1em;
> 				/*字体对齐方式   居左*/
> 				text-align: left;
> 				/*上内边距*/
> 				padding-top: 5px;
> 				/*下内边距*/
> 				padding-bottom: 4px;
> 				/*背景颜色*/
> 				background-color: #A7C942;
> 				/*字体颜色:前景色*/
> 				color: #ffffff;
> 			}
> 			/*table所有后端元素的tr并且是具有class属性值为alt的tr内的td元素*/
> 			#customers tr.alt td {
> 				/*前景色*/
> 				color: #000000;
> 				/*背景颜色*/
> 				background-color: #EAF2D3;
> 			}
> 			
> 			
> 			div{
> 				/*设置div的边框是1px宽,实线,对应的颜色*/
> 				border: 1px solid #0000FF;
> 			}
> 			
> 		</style>
> 	</head>
> 
> 	<body>
> 		<div>11111111111111111</div>
> 		
> 		
> 		<table id="customers">
> 			<tr>
> 				<th>Company</th>
> 				<th>Contact</th>
> 				<th>Country</th>
> 			</tr>
> 
> 			<tr>
> 				<td>Apple</td>
> 				<td>Steven Jobs</td>
> 				<td>USA</td>
> 			</tr>
> 
> 			<tr class="alt">
> 				<td>Baidu</td>
> 				<td>Li YanHong</td>
> 				<td>China</td>
> 			</tr>
> 
> 			<tr>
> 				<td>Google</td>
> 				<td>Larry Page</td>
> 				<td>USA</td>
> 			</tr>
> 
> 			<tr class="alt">
> 				<td>Lenovo</td>
> 				<td>Liu Chuanzhi</td>
> 				<td>China</td>
> 			</tr>
> 
> 			<tr>
> 				<td>Microsoft</td>
> 				<td>Bill Gates</td>
> 				<td>USA</td>
> 			</tr>
> 
> 			<tr class="alt">
> 				<td>Nokia</td>
> 				<td>Stephen Elop</td>
> 				<td>Finland</td>
> 			</tr>
> 
> 		</table>
> 	</body>
> 
> </html>
> 
> 
> 
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style type="text/css">
> 			
> 			
> 			div:hover{
> 				background-color: #0000FF;
> 				text-decoration: underline;
> 			}
> 			a:hover{
> 				background-color: #44FF55;
> 			}
> 			
> 			
> 			/*ul {list-style-type:circle}*/
> 			ul{list-style-type:square}
> 			ol{list-style-type:upper-roman}
> 			/*ol{list-style-type:lower-alpha}*/
> 
> 		</style>
> 	</head>
> 	<body>
> 		
> 		<ul>
> 			<li>111111111111</li>
> 			<li>222222222222</li>
> 			<li>333333333333</li>
> 			<li>444444444444</li>
> 		</ul>
> 		<ol>
> 			<li>111111111111</li>
> 			<li>222222222222</li>
> 			<li>333333333333</li>
> 			<li>444444444444</li>
> 		</ol>
> 	
> 		
> 		
> 		<a href="05-div.html">05050505</a>
> 		<div>11111111111111111111</div>
> 		<div>22222222222222222222</div>
> 		<div>33333333333333333333</div>
> 		<div>44444444444444444444</div>
> 	</body>
> </html>
> 
> 
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		
> 		<!--css代码往哪里写？
> 			1、在style元素中编写：样式可以作用于当前的html文件，若你想让多个html文件公用一个样式的话，就必须使用独立的css文件
> 			2、独立的css文件中：可以让多个html文件公用一个css样式
> 			3、在html元素的style属性中编写::作用范围仅仅是对应的html元素
> 		-->
> 		
> 		<style type="text/css">
> 			div{
> 				/*设置背景颜色*/
> 				background-color: #AA9900;
> 			}
> 			
> 			#id1{
> 				width: 400px;
> 				height: 400px;
> 				/*设置背景图片*/
> 				background-image: url(img/a1.jpg);
> 			}
> 			p {text-indent: 5em;}
> 		</style>
> 	</head>
> 	<body>
> 		<div style="background-color: #0000FF;">33333</div>
> 		
> 		<div id="id1">4444444</div>
> 		
> 		<p>111111111111111111111111111111111111111111111啊十大法师法师发生的发sf啊时代发生的发撒旦发生的发生的发生的发顺丰撒发生是的个法师法发的发生的发发大厦1</p>
> 		<p>22222222222222222222222222222222222222222222222222</p>
> 	</body>
> </html>
> 
> ~~~
>
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--
> 			link:引用独立的css文件，这样这个css文件中的样式就可以运用到当前html页面上了
> 			href:指定目标css文件的url
> 		-->
> 		<link rel="stylesheet" type="text/css" href="css/mycss.css">
> 	</head>
> 	<body>
> 		<div>111111111</div>
> 	</body>
> </html>
>
>
> ~~~html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style type="text/css">
> 			
> 			div{
> 				/*宽度*/
> 				width: 200px;
> 				/*边框的宽度是 20px 实线  #0000FF*/				
> 				border: 20px solid #0000FF;
> 				/*内边距  ：内容与边框之间的距离*/
> 				padding: 20px;
> 				/*外边距：变宽以外的和其他元素对应外边距的距离*/
> 				margin: 30px;
> 			}
> 			div{
> 				width:50px;
> 				border: 1px solid #FF00FF;
> 				/*上内边距*/
> 				padding-top: 10px;
> 				/*右内边距*/
> 				padding-right: 20px;
> 				/*下内边距*/
> 				padding-bottom: 30px;
> 				/*左内边距*/
> 				padding-left: 40px;
> 				/*上外边距*/
> 				margin-top: 10px;
> 				/*右外边距*/
> 				margin-right: 20px;
> 			}
> 			div{
> 				/*如下设置内边距,因为有方向的区分,所以如下样式是:上内边距和右内边距和下内边距和左内边距都是20px*/
> 				padding: 20px;
> 				/*上内边距是10px   右内边距是20px  下内边距是30px  左内边距是40px*/
> 				padding:10px 20px 30px 40px;
> 				/*上下内边距都是10px   左右内边距都是30px*/
> 				padding:10px 30px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		
> 		<div>111111111111111111111</div>
> 		
> 		<div>222222222222222222222</div>
> 	</body>
> </html>
> 
> ~~~
>
> 

## JavaScript

### 什么是javascript？

javascript是一个面向对象的基于浏览器的弱类型的脚本语言。

> ①、面向对象：js是可以创建对象
>
> ②、基于浏览器：js代码由浏览器负责解析执行
>
> ③、弱类型：强类型java就是一个强类型的编程语言，即在定义变量时必须指明当前变量是什么类型
>
> java：int age=10;//强类型
>
> js：age=10;
>
> ④、脚本语言：狭义的理解，js本身无法发挥其作用，必须依附在html页面的基础上才能发挥其作用。

### js代码往哪里写？

> ①、在独立的以js为扩展名的文件中编写
>
> ②、可以在script标记中编写
>
> A：写在head中
>
> B：写在body的最后面
>
> ③、可以写在html的事件中

### javascript中的基本知识

1、变量：是一个容器，其中保存的内容，叫变量的值，并且这个变量的值可以发生改变；变量实际上是一个临时性质的，即变量的值存储在内存中。

变量需要起一个名字，这个名字相当于内存中的地址一样，要想访问变量的值，必须通过变量名访问

2、数据类型：js中将不同类型的值划分为不同的类型。共有7个。***因为类型不同，操作方式也将不同。***

> 数值型：可以表达小数、整数、负数。30
>
> 布尔型：javaboolean类型，只有两个取值  false   true
>
> 字符型：用于表达一个或者多个字符序列   ，在js中字符型必须用  ''   或者  “”括起来.   ’刘备‘ | “刘备”
>
> 数组型：用于存储和管理多个相同类型的数据。   
>
> 对象型： String  Number 等基本类型
>
> null：      空的对象
>
> undefined：未定义的对象。

### javascript中的运算符

> ①、算数运算符： +   -   *   /   %  
>
> ②、赋值运算符：=  将=符号右面的部分的值赋给左面的变量     var  age=30;   将30的值赋给了age变量
>
> ③、算数赋值运算符：   +=    -=   *=   /=    %=
>
> ④、增量减量运算符：  ++    --；一定要注意增量和减量运算符的两种使用形式
>
> A：前缀形式      运算符在变量之前    叫前缀      ++a;   
>
> 前缀形式  先把自己+1 然后将结果拿出去参与其他的运算
>
> B：后缀形式      运算符在变量之后    叫后缀      a++;
>
> 后缀形式  先把自己拿出去参与其他的运算之后在把自己的值+1；
>
> ⑤、关系|比较运算符：<    <=   >   >=   ==等于   !=不等于
>
> 注意：关系运算符的运算结果是boolean类型。也就是true   |  false   
>
> ⑥、逻辑运算符：  &&与   ||或    !反
>
> ⑦、条件运算符：？  ：　组成
>
> 

~~~ html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		
		<style type="text/css">
			/*都是css代码,即这里代码的语法规则必须按照css的规则编写*/
		</style>
		
		
		<script type="text/javascript">
			//都是js的代码，即这里的代码都必须按照js的语法规则编写。
//			定义变量  var是一个关键字，专门用于定义变量
// 			语法：var 变量名=初始值;
			var age=30;//在内存中申请一片空间，其中的值是30  变量的名叫age，所以要操作30这个值就必须通过age变量名我完成
			age=40;// 对age名对应的内存空间的值重新设置为40;
			
//			将age内存中的值打印到浏览器的控制台
			console.log(age);
			console.log(30);
//			弹出消息框,并在消息框中显示age变量对应内存中的内容
			alert(age);
		</script>
		
		
	</head>
	<body>
	</body>
</html>



<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		
		<script type="text/javascript">
			
			var age=10;
//			访问age变量的中值并加上10,然后将结果赋给了age1;
			var age1=age+10;
			var age2=age-3;
			var age3=age*3;
			//若有小数照样首先小数
			var age4=age/4;  
			var age5=age%3;//age 除以3  的余数返回给age5变量；
			console.log(age1);
			console.log(age2);
			console.log(age3);
			console.log(age4);
			console.log(age5);
			
			console.log("=================");
			var a=10;
			var b=20;
			
			b+=a;///  等价式：    b=b+a;   所以   b=20+10=30；
			console.log(b);
			b-=a;  ///  b=b-a;
			b*=a;  ///  b=b*a;
			///  b=b/a;
			b/=a;  
			b%=a; ///   b=b%a;
			
			
		</script>
	</head>
	<body>
		
	</body>
</html>



<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		
		<script type="text/javascript">
			var a=10;
			var b=10;
			a++;//  a++  等价式   a=a+1;   a=10+1=11;
			b--;//  b--  等价式   b=b-1;   b=10-1=9;
//			console.log(a);
//			console.log(b);
//			
			var c=10;
			var d=++c;//先把自己+1 然后将结果拿出去参与其他的运算   先把c+1  =11；然后将11赋值给了d
		
			var e=10;
			var f=e++;//先把自己拿出去参与其他的运算之后在把自己的值+1；  先把e的值10赋值给了f，然后在把e+1=11；
			console.log(d);// 打印11
			console.log(f);// 打印10
			
			console.log(c);
			console.log(e);
//			老对儿：同座   搭档  

			var g=10;
			var h=20;
			
			var i=g>h;//  10>20  false
			console.log(i);//打印false
			
			console.log(g==h);
			console.log(g!=h);
			
		</script>
	</head>
	<body>
	</body>
</html>


<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		
		<script type="text/javascript">
			var a=true;
			var b=false;
			// 真：true   假：false
			console.log(a&&b);//与  and  就是两个都为真时结果才为真
			console.log(a||b);//或   or   就是两个有一个为真，结果就为真
			console.log(!a);//  取反，，   也就是真返回假  假返回真
			
			
			var a=10;
			var b=20;
//			a>b吗吗?若大于的话,即结果为真的情况下,返回a,否则返回b
			var max=a>b?a:b;
			var min=a>b?b:a;
			
			console.log(max);
			console.log(min);
		</script>
	</head>
	<body>
	</body>
</html>

~~~

