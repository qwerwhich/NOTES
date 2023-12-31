<a name="iq13h"></a>
# 基础标签
**<h1>,<h2>,......,<h6>**<br />**<p>**<br />**<br>**<br />**（两句话用<p></p>分为两段的话 两句话垂直之间也存在距离 直接用<br>分开的话不会存在距离 **<br />**因为<p>表示的是一个段落 而<br>只是换行**<br />**<hr>**

<a name="X2iBV"></a>
# 文本格式标签
**加粗		b	or 	strong**<br />**下划线	u	or	ins**<br />**倾斜		i	or	em**<br />**删除线	s	or	del**

<a name="hFf51"></a>
# 基础内容标签
**图片<img**<br />**src	路径		alt	  失效时替换图片	  title	悬浮时显示文本**<br />**width  宽		higth  高  （只设置一个的话 另外一个会等比例改变**<br />**>**

**音频<audio		**<br />**src 	路径（相对路径用./接具体位置表示	./也可以省略		../表示返回上一级**<br />**controls   显示播放控件		autoplay  自动播放		**<br />**loop  循环播放>**<br />**</audio>**

**视频<video**<br />**src 	路径		controls   显示播放控件		autoplay  自动播放		**<br />**loop  循环播放>**<br />**</video>**

**超链接<a**<br />**href  目的网址（若为空可用'#'符号来代替**<br />**target 打开链接的方式 (_self表示覆盖原网页  _blank表示另开页 **<br />**不写target默认是_self**<br />**>**<br />**链接文字**<br />**</a>**

<a name="LBTtV"></a>
# 列表标签
**无序列表 		有序列表		自定义列表**<br />**（表标签只能包含项标签 项标签可以包含任意标签）**

**无序列表**<br />**<ul></>	（unorderlist）	代表整个无序列表**<br />**<li></>（orderlist）		代表列表中的项，前面默认带圆点标识**

**有序列表**<br />**<ol></>		代表整个有序列表**<br />**<li></>		代表列表中的项，前面默认带序号**

**自定义列表**<br />**<dl></>(definedlist)		代表整个自定义列表**<br />**<dt></>		代表自定义列表中的一个主题（一个列的表头）**<br />**<dd></>	代表主题里的内容项**

<a name="yJzoH"></a>
# 表格标签
**<tabel	border 边框宽度 	 width 表格宽 		height 表格高></>代表整个表格**<br />**<tr></> 代表行**<br />**<td></> 代表行内单元格**<br />**<caption></>表格标题**<br />**<th></>表头单元格 放在tr里，表头里的单元格用此表示**

**表结构标签**<br />**<thead></> 表头**<br />**<tbody></> 表主体**<br />**<tfoot></> 表结尾**<br />**三个标签不起直观作用，用于增强代码的可阅读性，加快浏览器译码**

**单元格的合并 （作为单元格的属性标签，依据左上原则，上下合并留上，左右合并留左**<br />**rowspan 行合并，其值代表合并的总数**<br />**colspan 列合并**

**合并之后对应的单元格不用额外写了**<br />**例如第一行第一个单元格rowspan属性值为2 则第二行的单元格是直接从第二个开始的 第一个直接为第一行第一个单元格的值所以直接跳过**<br />**合并只能用于同一结构的单元格，thead不能与tbody单元格一起合并**

<a name="qg0TJ"></a>
# 表单标签
**（表单用于用户输入**

<a name="TdbfG"></a>
## 表单标签input
**<input 	type输入类型> </>**

**type类型：**<br />**text 文本输入框**<br />**password 密码输入框**<br />**radio单选选择（前面带圆圈标识）**<br />**checkbox多选选择（带方形标识）**<br />**file上传文件按钮（只能上传一个）  **<br />**submit 提交按钮 提交数据到后端**<br />**reset 重置按钮，使表单恢复默认值**<br />**botton 普通按钮，配合js使用**

**用于配合text/password使用的额外属性：**<br />**placebolder 输入框占位符，用于提示输入框输入信息类型**

**用于配合radio使用的额外属性：**<br />**name 分组，其值为组名 用于单选选择 只有将单选的所有选择都放进同一个组 才能保持只有一个选择被选中		**<br />**checked 加了此属性，单选中默认选中此选择**

**用于配合file使用的额外属性：**<br />**multiple 使文件上传由单选变为多选 **

**用于配合按钮使用的额外属性：**<br />**value 定义按钮名字**

**表单域标签<form></> 套住整个表，重置按钮只有在具体form中才能有效**

<a name="AEWBW"></a>
## 按钮
（**按钮的另一种写法**<br />**<botton type="submit/reset/button">按钮的名字</> **

<a name="FfmS9"></a>
## 下拉菜单
**<select></>代表整个下拉菜单**<br />**<option  selected默认选中></>菜单的选项**<br />**与列表类似 select只能包含option**

<a name="crOYm"></a>
## 文字域
**<textarea  rows 高 cols宽></> 用于输入多行文字**

<a name="gmyTi"></a>
## 单选选择的额外功能
**(使点击单选圆圈标识旁边的字也能选中选择**<br />**两种方法：**

**1，兄弟关系 在input标签后额外增加lable标签使lable的id属性等于input的id属性**<br />**2，父子关系 用lable标签包含整个单选标签<input>**

<a name="zWsc9"></a>
# 语义化标签
<a name="Z3VZY"></a>
## 无语义的标签
**（即仅用于网页布局，无实际特殊结构与意义**<br />**<div></> 一行一个div  独占一行**<br />**<span></>一行多个span**<br />**用div装文本相当于自带换行的一行文本**

<a name="BHstq"></a>
## 有语义标签
**(用于手机端的网页制作，相关标签代表对应结构**<br />**<header></>**<br />**<nav></>**<br />**<aside></>**<br />**<article></>**<br />**<section></>**<br />**<footer></>**

<a name="mfPGI"></a>
## 字符实体
**html中不能识别多个连续空格，多个连续空格只会被判定为一个空格**<br />**所以可以使用"&nbsp;"来代替空格 起到转义符的作用**



