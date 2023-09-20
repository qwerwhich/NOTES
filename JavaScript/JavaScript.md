<a name="cn1eg"></a>
# JS简介
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1695137480577-3dfd120d-511a-405d-862a-9e3d17db804d.png#averageHue=%23fafdfa&clientId=uf3dd6c10-16db-4&from=paste&height=547&id=u8834ab65&originHeight=881&originWidth=925&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=252889&status=done&style=none&taskId=u86919b47-a790-4f38-9420-0e0b8312663&title=&width=574.178955078125)

<a name="THeHF"></a>
# JS位置
**JS与css一样有三种引入方式，包括内嵌，外联，行内式**<br />**内嵌式为将<script>（存放JS语句）</>标签写在body内，一般将script标签写在**<br />**body底部，因为网页代码的加载顺序是自上而下的，而script需要有前置标签才能**<br />**起作用，所以一般放最后**<br />**外联式为<script srt="xxx.js">（中间不能添加内容，否则会失效）</>，**<br />**将此标签同样写在body的底部，通过引入js文件添加JS效果**<br />**行内式与css一样，直接在想要添加JS效果的标签内作为属性添加JS属性**<br />**比如<button onclick="alert('警告警告')">这是按钮的文本</button>**

<a name="uEOZI"></a>
# JS的输入与输出
<a name="CQ44R"></a>
## 输出
<a name="dcqSW"></a>
### 1，document_write('文字或标签')
**此输出的显示方式与一般的标签相似，显示在页面内**<br />**括号里的内容可以为文字或者标签**<br />**标签能生效，如果是文字则默认为div标签效果**
<a name="fGF5j"></a>
### 2，alert('')
**输出方式与标签不同，不显示在页面内，而显示在页面上方**
<a name="iYx3f"></a>
### 3,console.log('')
**此输出只有程序员可见，显示在调式台里，一般用于开发日志**
<a name="g8jbF"></a>
## 输入
<a name="KE5yw"></a>
### prompt('文字')
**在页面上方显示一个输入框，文字内容用来提示用户输入什么内容**

**alert于prompt能跳过渲染直接执行，因为他们显示在页面上方**
