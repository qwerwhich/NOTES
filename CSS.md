<a name="LpFr3"></a>
# 简述
**css有三种引入方式，包括内嵌式，外联式，行内式**<br />**（css中的注释形式与html不同，与c，c++形式相同**<br />**写css要从外到内，先宽高背景色，再放内容，调节内容位置，控制文字细节**
<a name="Y5Ms8"></a>
## 内嵌式
**内嵌式为在html文件中的head标签中title标签后添加一个<style></>标签**<br />**style标签中的格式为**<br />**选择器{**<br />**······；**<br />**}**<br />**选择器可以是标签的名字**<br />**通过此方法给特定标签修饰**<br />**例如**<br />**<style>**<br />**p{**<br />**color:red;//代表将p中的文字颜色改为红色**<br />**background-color:green;//一个标签有他自己的域（也即背景），例如一个p的标签的域就是他所在的那一整个行 background-color改变的就是域的颜色**<br />**fontsize:60px;//定义p中字体大小,px代表像素**<br />**width：600px；//改变p标签域的宽度**<br />**height: 500px;//改变p标签域的高度**<br />**}**<br />**</style>**

<a name="gIImC"></a>
## 外联式
**通过在html文件外部建立.css文件来引入css**<br />**此方法需要在head标签中title标签后添加link标签，herf后面接.css文件所在的相对路径**<br />**css文件中可以直接编码**<br />**即**<br />**选择器{**<br />**······；**<br />**}**<br />**格式**

<a name="yOYjP"></a>
## 行内式
**行内式如其名，在标签中使用style属性对其进行css修饰**<br />**如<p  style="color:red;  fontsize:60px; ······;"></p>**<br />**来添加css**

<a name="c1Yf6"></a>
# 选择器
**基础的选择器有 标签选择器，类选择器，id选择器，通配符选择器**
<a name="VDgSn"></a>
## 标签选择器
**格式为 **<br />**<标签>{**<br />**······；**<br />**}**<br />**以标签命名的选择器，会对所有选中的标签生效**

<a name="Dtpt6"></a>
## 类选择器
**格式为**<br />**.类名{**<br />**······；**<br />**}**<br />**每个标签有一个类属性 class 与c++类似，所以可以通过类来给标签添加css**<br />**一个标签可以属于多个类**<br />**如**<br />**<p calss="类名1 类名2 ······"></>**

<a name="sdAzk"></a>
## id选择器
**格式为**<br />**#id{**<br />**······;**<br />**}**<br />**每个标签有一个id属性可以唯一标识此标签 所以也可以通过id来为标签添加css**<br />**用法如下：**<br />**#ficd{**<br />**······；**<br />**}**<br />**<p id="ficd"></>**

<a name="oeCfl"></a>
## 通配符选择器
**格式为**<br />***{**<br />**······;**<br />**}**<br />**作用是对所有的标签进行css修饰**<br />**用的比较少 一般只用于调节字体的margin 与 padding属性**
<a name="rt4EM"></a>
# 
<a name="fJxd4"></a>
# 文字和文本样式
<a name="TVFdk"></a>
## 文字
**css中常见的用于调节文字的关键词有**<br />**font-size 字大小,font-weight 字粗细,font-style 字倾斜,font-family 字体**
<a name="uePB2"></a>
### font-size:
**单位为px**<br />**默认字体大小为16px**

<a name="iSxd0"></a>
### font-weight:
**无单位，可以用关键字来赋值，也可以用数字赋值**<br />**关键字有 normal 正常，bold 加粗**<br />**对应数字赋值里的 400，700**

<a name="hNXCJ"></a>
### font-style:
**关键字赋值**<br />**有 normal 正常，italic 倾斜**

<a name="JepaR"></a>
### font-family:
**用字体名字进行赋值**<br />**字体有很多种，分为非衬线字体，衬线字体，等宽字体**<br />**非衬线字体有微软雅黑，黑体，...... 用于网页 **<br />**衬线字体有宋体，楷体，...... 用于报纸**<br />**等宽字体多半用于编程**<br />**可以用多个字体名字对font-family进行赋值**<br />**如下**<br />**font-family: 微软雅黑，黑体，san_self；**<br />**(san_self即非衬线字体)**<br />**当用户浏览网页时假如电脑不支持微软雅黑会换到黑体**<br />**如果黑体也不支持会换到用户电脑支持的一个非衬线字体**

<a name="GOrKk"></a>
### 扩展：
**css具有层叠性，当同一个标签的关键词用多个不同的关键字修饰时**<br />**后面的会覆盖前面的**<br />**如**<br />**<p>{**<br />**color:red;**<br />**color:green;**<br />**}**<br />**最后p字体颜色会为green**

**font也可以作为复合属性出现在css中**<br />**用法为 font：style,weight,size/line-hight,family**<br />**使用这种复合属性时必须按照此顺序写**<br />**只有style，weight可以省略 **<br />**如果要规定line-hight（行高）就必须在size后面加/**<br />**行高有 数字+px, 数字  两种写法**<br />**第一个是以像素为单位，第二个是以当前标签字体大小为单位**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1690515094912-587d959b-b40a-4f0a-8139-324d05db64f4.png#averageHue=%23e2e3e2&clientId=u4b4df3c9-ba51-4&from=paste&height=126&id=u78bcaeef&originHeight=139&originWidth=396&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=45887&status=done&style=none&taskId=ueba6b3c3-f6d2-4491-8ee7-fd7f063a2c6&title=&width=359.9999921972103)

<a name="l6LzX"></a>
## 文本
<a name="MdG8o"></a>
### text-indent:
**文本缩进(即设置每个段落前面的空行）		**<br />**单位有px与em**<br />**px即像素		em为单位字，即当前标签规定的字体大小**

<a name="YrCBP"></a>
### text-align:
**水平对齐 **<br />**其值为 left/center/right 分别代表左水平对齐，中心对齐，右水平对齐**<br />**其中居中对齐得对想要居中对齐的元素的父元素设置text-align:center 才会居中对齐**<br />**例如**<br />**<body>**<br />**<img></img>**<br />**</body>**<br />**想让img居中对齐得在css中给body标签添加text-align:center**

<a name="HJtAM"></a>
### text-decoration:
**text-decoration 为文本修饰**<br />**text-decoration： underline 下划线/line-through 删除线/overline 上划线**<br />**/none 无装饰线**<br />**对超链接使用无装饰线可以去除超链接的下划线**

<a name="jZiQF"></a>
### 扩展:
**为了使标签的域居中 可以使用margin: 0 auto**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1690514703705-0969fb85-05c3-4114-8d7c-10d5f7ce60d6.png#averageHue=%23222121&clientId=u4b4df3c9-ba51-4&from=paste&height=390&id=u2abfec0a&originHeight=512&originWidth=659&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=180835&status=done&style=none&taskId=u06790fcc-b48d-49e7-bf62-abb03a776eb&title=&width=502.07952880859375)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1690514679365-026be5b2-b4ec-4bbb-95f1-f41878349c8a.png#averageHue=%23fefefe&clientId=u4b4df3c9-ba51-4&from=paste&height=270&id=u0b08ef14&originHeight=542&originWidth=1010&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=57904&status=done&style=none&taskId=u2de1615b-fc8b-4130-b04d-fb8c9235def&title=&width=503.178955078125)
<a name="ETd1Q"></a>
### <br />

<a name="Z7III"></a>
# 复合选择器
<a name="V1okb"></a>
## 后代选择器
**格式为  **<br />**选择器1 选择器2{**<br />**······；<br />}**<br />**网页会将选择器1选中的标签中的后代（子，孙，··）选择出符合选择器2**<br />**的标签，对其进行css修饰**
<a name="Ng1eG"></a>
## 子代选择器
**格式为**<br />**选择器1>选择器2{**<br />**······；**<br />**}**<br />**会将选择器1选中的标签的子标签中选择出符合选择器2的标签，对其进行修饰**
<a name="y29rS"></a>
## 并集选择器
**格式为**<br />**选择器1，选择器2{**<br />**······；**<br />**}**<br />**能将选择器1选中的标签与选择器2选中的标签都进行修饰**
<a name="YPhwI"></a>
## 交集选择器
**格式为**<br />**选择器1选择器2{**<br />**······；**<br />**}**<br />**两个选择器直接写在一起**<br />**只会讲既满足选择器1又满足选择器2的标签进行修饰**
<a name="SSSm8"></a>
## 伪类选择器
**格式为**<br />**选择器1：hover{**<br />**······；**<br />**}**<br />**此选择器并不会对满足选择的标签的内容直接进行修饰**<br />**而是会对鼠标悬浮在此标签上的内容时进行修饰**<br />**比如一般鼠标悬浮在超链接上时，超链接会变红，就是此选择器的作用**
<a name="WAyPI"></a>
## emmet
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1690550957872-447bc8d9-49e0-496f-9541-4e35fb667510.png#averageHue=%23f7f7f7&clientId=u270b5f2e-2b03-4&from=paste&height=408&id=uec36eb3d&originHeight=449&originWidth=985&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=187823&status=done&style=none&taskId=u507039e7-8bfd-470c-9e0a-38e3d559731&title=&width=895.4545260460912)<br />**“+”：colo+bgc+heig 可以变成 color: ; background-color: ; hegiht: ;**<br />**p.red 会创建标签<p class="red"></p> 如果直接写.red会默认产生div标签**<br />**其他也一样默认为div标签**


<a name="Ppnj0"></a>
# 背景
<a name="nGT5p"></a>
## 背景色
**background-color: ;**
<a name="gwCxv"></a>
## 背景图片
**background-image: url();**

<a name="uO9c5"></a>
## 背景图平铺
**背景图是以左上为起点出现在标签域当中的**<br />**如果背景图比域小 可以选择用多个背景图将其平铺满**<br />**background-repeat:**<br />**repeat 默认值，水平垂直方向都平铺**<br />**no-repeat 不平铺**<br />**repeat-X 只水平铺**<br />**repeat-Y 只垂直铺**

<a name="jt9uY"></a>
## 背景图位置
**background-position**<br />**两种取值，一种是关键词取值，一种是数字取值（背景图片默认为left,top/0px,0px）**<br />**left/center/right(水平方向),top/center/bottom(垂直方向)**<br />**x px,y px**

<a name="zcrGh"></a>
## 扩展
**类似于font**<br />**background也可以用复合属性表示**<br />**background： color，image，repeat，position**<br />**不过background不像font一样有顺序要求，它不分顺序**
<a name="wBuF2"></a>
# 
<a name="OtVdG"></a>
# 元素显示模式
**元素显示模式分3种为 块级元素，行内元素，行内块元素**
<a name="NBFaC"></a>
## 块级元素
**类似于div，p 等标签**<br />**独占一行，宽高可以设置**
<a name="TAFMq"></a>
## 行内元素
**类似于span strong em 等标签**<br />**一行多个，不可以设置宽高，宽高由内容决定，即由内容撑开**
<a name="Wmrag"></a>
## 
<a name="ZfLXf"></a>
## 行内块元素
**如input，textarea,button等**<br />**一行多个，可以设置宽高**
<a name="gRFOv"></a>
## 
<a name="QSRS1"></a>
## 元素显示模式的转换
**display：block 转变为块级元素/inline 转变为行内元素/**<br />**block-inline 转变为行内块元素；**

<a name="UFPqv"></a>
## 扩展
**块级元素内可以套行内，行内块元素**<br />**如**<br />**<div>**<br />**<span>	</span>**<br />**</div>**

**块级元素内不能套块级元素，行内元素不能套块级元素**
<a name="tdXeN"></a>
# 
<a name="H43hL"></a>
# css三大特性
<a name="CP9Nu"></a>
## 继承
**只有控制文字的一些标签才能继承**<br />**即对父标签标明css属性 其后代会继承其css属性**<br />**不过假如其后代本身具有同类不同值得属性，会覆盖父类的，以自己的为主**<br />**div{**<br />**color:red;**<br />**}**<br />**<div>**<br />**<a> </a>**<br />**</div>**<br />**父类div的颜色为红色，不过a为超链接，它本身的颜色为蓝色，所以蓝色会覆盖红色**<br />**假如a标签换为别的本身没颜色的标签但是用css标明了颜色，此颜色也会覆盖父类的颜色**
<a name="RjiQd"></a>
## 层叠
**标签选择器，类选择器，id选择器的优先级各不同**<br />**选择器优先级一致的才会层叠，不然低优先级会被高优先级选择器覆盖**

<a name="BU3YD"></a>
## 优先级
**继承<通配符选择器<标签选择器<类选择器<id选择器<行内样式<!important**<br />**(!important 加在属性后面，分号前面，将其优先级提到最高，但对继承无效**

**权重叠加**<br />**对于复合选择器而已，因为可能由多种选择器组成，因此不能轻易的判别其优先级**<br />**需要对其权重进行叠加，权重相同则按层叠性来**<br />**权重计算按(行内样式，id选择器，类选择器，标签选择器)来比较**<br />**前面的值大则权重大，相同则比较下一个值**<br />**比如(1,0,0,0)就比（0,10,10,10）大**

**示例：**<br />**.c1 .c2{**<br />**color:red;**<br />**}**<br />**.c1 #id2{**<br />**color:green;**<br />**}**<br />**div p{**<br />**color:black;**<br />**}**<br />**#id1{**<br />**color:white!important;**<br />**}**<br />**<div class="c1" id="id1">**<br />**<p class="c2" id="id2">文本</p>**<br />**</div>**<br />**选择器的权重分别为(0,0,2,0) (0,1,1,0) (0,0,0,2) (0,1,0,0)**<br />**虽然最后一个选择器有!important对于div权重最高 但是他是div的选择器**<br />**p从他那获得的方式是继承 因此对于p而言权重最低**<br />**因此对于p而言权重最高的是第二个选择器 因此文本的颜色应该为green**<br />![~DN]3NBA7HCG3BUKWMX1SP1.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1690869352414-55e5d759-9dd7-4bd5-8a2b-98d3538ca721.png#averageHue=%23a2a2a2&clientId=u1ef5823d-aa0c-4&from=drop&id=ub2bd826c&originHeight=845&originWidth=1717&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=283900&status=done&style=none&taskId=ua8eee6a6-144a-4658-a120-32f45a27226&title=)


**范围越精准，优先级越高**<br />**如果同样是继承，那么优先级取决于继承于哪个长辈，继承的长辈离自己越近优先级**<br />**越高，就近原则	就像是相比你爷爷的话你更听你老子的话**

<a name="dxmtr"></a>
# 盒子模型
**网页中的每一个元素都是一个盒子**<br />**每个标签都可以看做是一个盒子**

**就像一个装着电脑的快递盒子一样盒子分为三层**<br />**分别是 电脑（内容 content） 泡沫（内边距 padding） 纸壳（外边距 border）**<br />**与其他快递盒子的距离（盒子间距 margin）**<br />**盒子尺寸包括内容，内边距，外边距**
<a name="sQoA8"></a>
## 内容 content
**width ,height 设置宽高**

<a name="mAA2O"></a>
## 内边距 padding
**padding： 10px；（设置上下左右四个内边距均为10px**<br />**也可以作为复合属性写多个值： padding： 10px 12px 23 px 34px;**<br />**分别为上右下左的内边距，即顺时针**<br />**也可以单独设置 padding-top/left/right/bottom: x px;**

<a name="Qscyn"></a>
## 外边距 border
**复合属性 border：width style color; （分别为外边距大小，线的样式，线的颜色**<br />**顺序随意）**<br />**常见线的样式有 solid 实线，dashed 虚线，dotted 点线 **<br />**border: 10px solid black;（边框长10px 实线 黑色）**<br />**border属性是对上下左右四个方向设置相同的属性**<br />**想要单独设置一边 需要用到 border-top/left/right.bottom: 	;**

** **
<a name="ugvj0"></a>
## 盒子间距 margin
**和padding一致**

<a name="NZLLv"></a>
## 一些其他知识
<a name="Zjle4"></a>
### 清除默认间距：
**有一些标签会默认带有内边距或者盒子间距**<br />**为了避免这些默认间距对布局的影响 在css的开头会用通配符选择器清除默认间距**<br />***{**<br />**margin：0；**<br />**padding：0；**<br />**}**

<a name="hPvgP"></a>
### 版心居中：
**在之前学的标签居中**<br />**margin：0 auto； 其实就是设置盒子距离 上下为0，auto代表左右间距相同；**

<a name="fj8I6"></a>
### 内减属性：
**为了直接用width和height设定盒子尺寸可以用内减属性 **<br />**box-sizing：border-box；**

<a name="IIFNI"></a>
### 去除列表符号：
**无序列表和有序列表的li前面都有一个符号，圆圈标识或者排序**<br />**可以用**<br />**ul{**<br />**list-style：none；**<br />**}**<br />**来去除列表符号；**

<a name="DzkcV"></a>
### 块级元素和行内元素存在的问题
**块级嵌套存在的合并现象：**<br />**两个块级标签，一个有下盒子间距，一个有上盒子间距**<br />**最终两个盒子的间距会取两个值的最大值，而不是两值之和，这就是合并**

**块级嵌套存在的塌陷现象：**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1690967140042-a10ef768-cd05-4ce6-8b88-f51c93ab4b69.png#averageHue=%23f3f3f3&clientId=u32c89a16-72a9-4&from=paste&height=352&id=u5c1fe2a6&originHeight=387&originWidth=1046&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=146355&status=done&style=none&taskId=u704b077b-b54a-49a2-ae54-0fe5a1be8e5&title=&width=950.9090702986919)<br />**一般通过给父元素设置overflow：hidden来解决塌陷问题**

**行内元素的内外边距问题：**<br />**行内元素的内外边距在垂直方向不生效**<br />**可以通过给字体设置行高来解决**

<a name="cjtq5"></a>
## 结构伪类选择器
**对于一个包含多个子标签的父标签，倘若想要选中此父标签的某一个标签**<br />**可以使用结构伪类选择器**<br />**格式为**<br />**E: first-child{} E为子标签名称，选中第一个子标签**<br />**E:last_child{}  选中最后一个子标签**<br />**E:nth-child(n){} 选中第n个子标签**<br />**E:nth-last-child(n){} 选中倒数第n个子标签**

**E:nth-child(n){}与E:nth-last-child(n){} 中的n也可以换成公式**<br />**n为2n则表示选中偶数类子标签 **<br />**n为2n-1表示选中奇类子标签**<br />**-n+5表示选中前五个子标签（因为n是从0开始往后加**<br />**n+5表示选中从五开始的子标签**

<a name="FiHMb"></a>
## 伪元素
**通过css创建的假标签**<br />**例如一些装饰性的不重要小图就是用伪元素达成的**<br />**伪元素默认为行内元素**<br />**格式为	E：before/after{**<br />**content：;（必须有此元素 可以通过“”或者''符号在里面添加文本显示出来**<br />**就算不打算加文本也要有此元素 其值为空，不加此元素不生效**<br />**}**<br />**before表示在E标签前面显示，after表示在E标签后面显示**

**但好像仍然是在E标签的盒子里面显示,也就是before和after好像是在E里面的第一个内容前和E里面的最后一个内容后显示**

<a name="Lsb7I"></a>
## 标准流
**指的是 标签默认排列方式**<br />**比如 div标签一行只能排一个，且会换行，span一行可以排多个**<br />**这就是其标签的标准流**

<a name="XfSOJ"></a>
# 浮动
<a name="YBCiD"></a>
## 浮动的基本特点
**浮动用于网页布局**<br />**将两个div标签的显示模式转换为行内块**<br />**如果两个div用换行隔开 则两个div之间会有一个空格间距，写在一行又不美观**<br />**不宜于阅读 所以不使用换关系模式来使得多个div共处一行，而是选择用浮动来解决**<br />**因为存在此问题，所以一般用浮动代替关系模式转换**

**浮动最初用于图文环绕，后用于网页布局**<br />**格式为 **<br />**float：left/right；**

![}S0FRX3}ZPDY{0[EG_[E)UH.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691049605136-b076a5a2-95e3-4a11-a648-90054c3885fc.png#averageHue=%23f4f4f4&clientId=u1db97fa0-d4bd-4&from=drop&id=u01075ef2&originHeight=756&originWidth=1586&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=299173&status=done&style=none&taskId=u4eb52e98-90dc-4924-9bc0-3e54bffc820&title=)<br />**浮动标签顶对齐，浮动后的标签具有行内块的特点**<br />**css书写顺序**<br />**1，浮动/display**<br />**2，盒子模型（margin，padding，border，width，height，bgc）**<br />**3，文字样式**

**主导航一般用 li+a 标签实现**

<a name="LCV8S"></a>
## 清除浮动（清除浮动带来的影响
**浮动有时会带来一些不好的影响**<br />**当父子级标签，子级标签浮动，而父级标签无高度时，子代不能撑开父级**<br />**造成后面的标准流会挤上来，占据父级标签的位置**

**解决方法有一下五种：**<br />**1，给父标签加高度，不过一般不这样使用，因为一些放资源的版块的高度**<br />**是不定的，资源会随着加载变多**<br />**2，添加额外标签，在父级版块内的最后额外添加一个块级子标签。且这个块级标签**<br />**的css里面包含一个属性 clear：both；**<br />**3，单伪元素清除法，实质上与第二种方法殊途同归，添加一个父级标签的after伪元素**<br />**且在此伪元素种使用clear：both；**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691050536702-4075c69f-e579-4b70-9601-6db266ee8fcd.png#averageHue=%23dddcdc&clientId=u1db97fa0-d4bd-4&from=paste&height=425&id=u7c3e7f34&originHeight=467&originWidth=1185&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=204145&status=done&style=none&taskId=u74329aaa-7efb-4d26-8fce-1a1d324289b&title=&width=1077.2727039234703)<br />**4，双伪元素清除法，此方法是单伪元素的改进，不仅能解决浮动问题还能解决块级元素**<br />**的塌陷问题，即添加一下代码：**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691050474633-4dcfdeb3-08fd-4672-90f6-c61d68447bad.png#averageHue=%23504839&clientId=u1db97fa0-d4bd-4&from=paste&height=283&id=u0c976226&originHeight=311&originWidth=356&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=89341&status=done&style=none&taskId=ubcb7810d-8598-4d81-a3b7-50f4df53e06&title=&width=323.63635662173454)<br />**只需要给出现浮动问题的父标签添加一个 clearfix类就能解决了；**<br />**5，给父级标签css添加一个额外属性： overflow：hidden； 此方法同样能解决浮动**<br />**和塌陷问题，不过更多还是使用伪元素方法，因为伪元素方法构成一个类，可供多个浮动问题解决时使用；**

<a name="hz9d7"></a>
## 扩展
**设置文本框内的提示字样式**<br />**input:placeholder{**<br />**color: ;**<br />**font-size: ;**<br />**}**

**img{**<br />**vertical-align： ；调整图片垂直对齐方式，其值为middle时使图片位于所在盒子垂直方向的中心位置**<br />**} 	**

<a name="aSX6f"></a>
## ！！！：
**1，先观察内容的范围确定盒子大小，再通过margin将盒子调整至该到的位置；**<br />**2，写一个标签的css时要注意以后会不会影响到同名的标签 例如一个范围里面有多个div 那么对一个div进行css修饰时，最好给这个div加一个类，不然光用后代选择器很容易影响到同级其他div标签；或者在写复合选择器时可以通过多用子代符号>来写选择器，这样也能缩小选择器选择范围，防止影响其他同名标签；**<br />**3，浮动的优先级高于margin，比如在一个盒子内有一个子盒子，子盒子设置浮动**<br />**float:left; 且设置margin：0 auto;		一个是左浮动，一个是居中**<br />**最后子盒子会处于父盒子的最左边，因为浮动优先级高于margin;**

<a name="sIIMx"></a>
# 布局方式
**布局方式一共有三种，包括前面讲过的标准流与浮动，最后一个是定位**<br />**优先级为 		标准流<浮动<定位**<br />**定位用于盒子之间的层叠与盒子的固定位置**<br />**定位的属性值有四种：**<br />**静态定位 static**<br />**相对定位 relative**<br />**绝对定位 absolute**<br />**固定定位 fixed**<br />**定位的使用方式为 position：属性值；+ 偏移量**<br />**偏移量用left/right： px; top/bottom: px;表示**

<a name="OARFZ"></a>
## 静态定位
**静态定位是默认的定位，也就是没定位，无作用**
<a name="Q3Ru1"></a>
## 相对定位
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691758990294-a56967f8-f26d-4cc3-8f51-36994bcd35d4.png#averageHue=%23f5f5f5&clientId=u1d93d83e-d86e-4&from=paste&height=325&id=u4bae5f1b&originHeight=357&originWidth=557&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=59289&status=done&style=none&taskId=u3b357ad4-acf2-4ed5-8b3f-16ff3029abd&title=&width=506.36362538850034)<br />**1，特点是相对自己原来的位置移动	；**<br />**2，不脱标（即仍然是一个标签，占据原来的位置）；**<br />**3，仍然具有标签原有的显示模式特点；**
<a name="nPH0Z"></a>
## 绝对定位
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691759262160-ba0780cd-42ef-42cf-966c-d48362b4c08c.png#averageHue=%23f5f4f4&clientId=u1d93d83e-d86e-4&from=paste&height=325&id=ub5ac6e20&originHeight=358&originWidth=637&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=65386&status=done&style=none&taskId=u0a3316c4-e4c1-4953-a589-b23cc90975d&title=&width=579.0908965394519)<br />**1，特点是移动依据父标签，假如父标签有定位，则以父标签为参照物，长辈标签都没有定位，则以浏览器为参照物（广义上的，假如父标签不满足就看爷爷，一直往上找，就近原则）；**<br />**2，一般在设计中，想要将子标签设置为绝对定位，则将父标签设置为相对定位（子绝父相）**<br />**；**<br />**3，设置为绝对定位的标签具有行内块的特点；**<br />**4，脱标；**![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691986655649-1921be0a-c2be-42d8-a6f7-290163e77e93.png#averageHue=%232b3026&clientId=ua0d85cf9-5b7c-4&from=paste&height=110&id=u67189032&originHeight=121&originWidth=764&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=86758&status=done&style=none&taskId=u2be38f52-112a-4df7-84a9-46b9974dbad&title=&width=694.5454394915876)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691986685156-be94d82f-7ebc-4e6a-a8eb-e6ccb566bf91.png#averageHue=%232b3026&clientId=ua0d85cf9-5b7c-4&from=paste&height=125&id=u65092471&originHeight=138&originWidth=758&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=56750&status=done&style=none&taskId=u7c2cacf5-ebc0-40af-afbb-e2636405233&title=&width=689.0908941552661)

**一个问题：**<br />**绝对定位的盒子不能只使用margin：0 auto; 居中，因为定位会改变盒子的域**<br />**比如：**<br />**div{**<br />**position：absolute；**<br />**left：500px;**<br />**}**<br />**div一开始水平方向的域为整个浏览器的水平方向，但是因为绝对定位使得整个盒子向右移动了500px，所以盒子的域也向右移动了500px；**

**那怎么才能让绝对定位的盒子居浏览器的中间呢？**<br />**可以这样设置css**<br />**div{**<br />**position: absolute；//先绝对定位**<br />**left：50%；//令盒子的左框居浏览器的中间**<br />**top：50%；//令盒子的上框居浏览器的中间**<br />**margin-left：-（盒子宽一半大小）px；//让盒子左边距减少盒子一半的大小**<br />**这样盒子在水平方向就居中了**<br />**margin-top：- （盒子高一半大小）px；//这样盒子垂直方向也居中了**

**（或者可以写成 transform：translate（-50%，-50%）；即**<br />**盒子在水平方向，垂直方向都向反方向，也就是上和左位移自己大小的一半**<br />**只有一个值的话为水平方向）**<br />**}**
<a name="zwyxh"></a>
## 固定定位
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691985769808-58770e6e-8fb8-4fcd-a2fe-5aed4fa9dd1b.png#averageHue=%23f5f5f5&clientId=ua0d85cf9-5b7c-4&from=paste&height=318&id=u1ce6d42e&originHeight=350&originWidth=485&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=63534&status=done&style=none&taskId=ua9d51402-8f9d-432e-bca1-385a768282a&title=&width=440.9090813526439)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1691986749248-0ab5c44d-75e6-460e-98a2-e7d5c8b41afc.png#averageHue=%231e1e1e&clientId=ua0d85cf9-5b7c-4&from=paste&height=139&id=ucb4afc34&originHeight=153&originWidth=388&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=41656&status=done&style=none&taskId=u1ab405f8-d107-4b98-8061-81fbd249de1&title=&width=352.72726508211514)

**行内块与行内元素假如不设置宽的话那其宽为内容的宽，而不是像块级元素一样占据整个水平方向**<br />**层级关系：标准级<浮动<定位，如果都是定位，则按层叠来，后面的覆盖前面的**<br />**也可以通过给一个标签添加z-index属性设定此标签定位的优先级，默认优先级为0**<br />**数值越大优先级越高，只能配合定位使用**
<a name="e9q50"></a>
# <br />
<a name="y0rM1"></a>
# 装饰
<a name="e78nc"></a>
## 垂直对齐方式
**vertical-align： baseline 默认基线对齐方式/top 顶对齐/middle 中间对齐/bottom 底部对齐；**

**浏览器会将行内，行内块元素标签视为文字来基线对齐**<br />**图片的基线在图片的下方，所以图片和文字简单放一起底部并不会对齐**

**想要图片在父级里居中，得用line-hight+vertical-align：middle；**<br />**父级{**<br />**line-high：父级高；**<br />**}**<br />**子级{**<br />**vertical-align：middle；**<br />**}

**
<a name="PkpqG"></a>
## 光标类型
**curser：default 默认箭头/pointer 此标签内光标未小手，即超链接的光标/**<br />**text 工字型，即复制文本时的光标/ move 十字光标，即移动图片时的光标**

<a name="Ah48W"></a>
## 圆角边框
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692068529035-71fbea9b-6eb2-4979-8806-6434ae671f5b.png#averageHue=%23f8f8f8&clientId=u4fe35175-25d2-4&from=paste&height=409&id=u5eded3c0&originHeight=450&originWidth=907&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=57242&status=done&style=none&taskId=u9db75427-19ed-41b9-a5da-e7300a5ed06&title=&width=824.5454366739135)<br />**border-radius： 圆角半径 px**<br />**也可以像margin一样设置四个值，从左上开始顺时针设置值，如果值小于四个，则按**<br />**对角相等的原则，类似于margin的对边相等原则**

**正圆盒子的构成：**<br />**首先盒子必须是正方形，再添加属性 border-radius：50%/或者盒子尺寸的一半；**

**胶囊按钮的构成：**<br />**首先盒子必须是横向长方形，再添加属性 border-radius：盒子高度的一半；**
<a name="ZfuWH"></a>
## 溢出补分显示效果
![BFH9QP(6FY4BPN_A)`W5F`C.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692068460792-fda68a21-ff88-43bc-89aa-92a8af17d3cc.png#averageHue=%23d4c5c1&clientId=u4fe35175-25d2-4&from=drop&id=ueb32976a&originHeight=717&originWidth=1540&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=593691&status=done&style=none&taskId=ub2d3efe0-c6a5-4534-814b-c8191bceac3&title=)
<a name="A09iU"></a>
## 元素本身隐藏
**两种方式：**<br />**visibility：hidden； //占位隐藏，因为占位所以一半不用**<br />**display：none；//不占位隐藏**

**鼠标悬停在父级，子级才显示，示例：**<br />**<div><img></img></div>**<br />**img{**<br />**display：none；**<br />**}**<br />**div::hover img{**<br />**display:block;**<br />**}**

**类似于这种功能：**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692068989605-bf1b0f30-38bb-4988-b98a-92d6f69ebe9f.png#averageHue=%2350452e&clientId=u4fe35175-25d2-4&from=paste&height=315&id=u0ecc1c1a&originHeight=346&originWidth=1019&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=561203&status=done&style=none&taskId=uf2767a56-4e75-4dc9-8eaa-d63911e0186&title=&width=926.3636162852457)

<a name="eNhQ5"></a>
## 元素整体透明度
**opacity：0~1；//表示透明度 0代表完全透明，1代表完全不透明**

<a name="kxl0Y"></a>
## 精灵图
**在网页中为了减少服务器发送次数，降低服务器压力，提高服务器处理速度**<br />**将多个小图合成一个大图来传输，这个合成大图就被叫做精灵图**

**对于一个大精灵图 怎么取其中的一小部分使用呢？**<br />**一般采用这个大图做背景图（因为直接用大图做盒子的话会把盒子撑大）**<br />**然后通过background-position：水平位置px，垂直位置px；**<br />**来调整**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692090393752-a38fbb22-5688-4870-82f3-cb22750aa516.png#averageHue=%23f3f3f3&clientId=u77f2384d-d56c-4&from=paste&height=197&id=ua96d9cac&originHeight=217&originWidth=779&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=45825&status=done&style=none&taskId=uc163d23e-c0b0-4773-8713-36070b4eab7&title=&width=708.181802832391)<br />**因为不是盒子在动，而是精灵图在动 使精灵图的目标位置对准盒子 **<br />**因为盒子初始在精灵图最左上角那个位置 所以精灵图都是往左，往上移动，所以都是负值**<br />**一般还配合background-repeat：no repeat；使用，使背景图不平铺**

<a name="lhkn1"></a>
## 背景图大小
![V~{RJW71ZQBQ]CWJPY06NW7.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692088928311-da15f51b-f045-4ef0-a1d7-27628b413025.png#averageHue=%23f7f7f6&clientId=u77f2384d-d56c-4&from=drop&id=u1de82b04&originHeight=598&originWidth=916&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=173699&status=done&style=none&taskId=ucc8a15dc-d173-46aa-9679-49711940bfd&title=)
<a name="RsKHl"></a>
## 
<a name="DEa9O"></a>
## 盒子阴影
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692090837308-6a784fb5-14df-4d78-ab5b-25ef557d83bc.png#averageHue=%23f8f8f8&clientId=u77f2384d-d56c-4&from=paste&height=695&id=u58140a2b&originHeight=765&originWidth=1498&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=191407&status=done&style=none&taskId=u81bd3253-c7f6-40e8-90f7-e3b0d9fe014&title=&width=1361.8181523015683)
<a name="iiyKR"></a>
## 过渡
![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692090997183-de1961aa-65e3-4aa5-8eeb-dc6c81c6decc.png#averageHue=%23f4f4f4&clientId=u77f2384d-d56c-4&from=paste&height=733&id=ub6d93848&originHeight=806&originWidth=1113&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=249759&status=done&style=none&taskId=u33116b00-fd68-4bd1-8fee-5ea633e2c49&title=&width=1011.8181598876138)<br />**过渡就是让元素样式慢慢变化**<br />**过度一般配合hover使用 hover添加变化 transition指定变化的时间**<br />**transition标签直接添加给变化的元素本身而不是hover**<br />**若有一个标签有多个属性变化需要过渡，例如可以这样复合写：**<br />**transition： width 1s，background-color 2s；（都是1s过渡的话**<br />**可以写成 all 1s；）**

<a name="GJokK"></a>
## 骨架标签解释
**<!DOCTYPE html>//文档说明**<br />**<html lang="en">//指明网页语言为英文en，简体中文为zh-CN**<br />**<head>**<br />**    <meta charset="UTF-8">//指定字符编码为UTF-8**<br />**    <meta http-equiv="X-UA-Compatible" content="IE=edge">**<br />**//解决ie浏览器兼容性差的问题**<br />**    <meta name="viewport" content="width=device-width, initial-scale=1.0">**<br />**//设置宽度=设备宽度，移动端网页使用  **<br />**<title>Document</title>**<br />**</head>**<br />**<body>**<br />**    **<br />**</body>**<br />**</html>**

<a name="yMnEx"></a>
## SEO（收索引擎优化三大标签）
**title		（<title></title>）	指定网页标题**<br />**description	（<meta name="description" content="">）	指定网页简介**<br />**keywords   （<meta name="keywords" content="">）指定网页在收索引擎里的关键字**

**都是在head标签里的**
<a name="CkRAx"></a>
## 
<a name="OgIe3"></a>
## ico图标
**设置网页图标**<br />**<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">**<br />**根目录底下的favicon.ico图片文件就是网页的图标**

<a name="q878H"></a>
## 文件和目录
**前端工程 文件和目录规范，以小兔鲜网页示例：**
<a name="Q1kdw"></a>
## ![]0L{(A`~Y5`NY8R9KJFK}$J.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1692088870847-67bc344a-7dc6-477e-aa73-878bd2732cf1.png#averageHue=%23f2f1f1&clientId=u77f2384d-d56c-4&from=drop&id=u461d7f08&originHeight=463&originWidth=1228&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=267817&status=done&style=none&taskId=u8b72da09-03e0-4590-a80d-e03dc6df329&title=)
**xtx是小兔鲜的缩写，pc代表工作端**<br />**base.css 里面存放一些基础公共样式，例如使每个盒子的初始**<br />**内边距 外边距都为0，去除超链接的下划线，解决浮动问题等等；**

**边写边测试**<br />**先调位置，盒子模型  最后调文字样式**

**div{**<br />**line-hight:30px;**<br />**}**<br />**span{**<br />**font-size:16px;**<br />**}**<br />**<div>**<br />**<span>好好好</span>**<br />**</div>**<br />**最后span盒子的高度是字高16px，不会被行高撑开**<br />**而div盒子的高度是30px，会被行高撑开 因为span是行内，div是块级标签**

**如果行内块和行内文字无法通过vertical-align或者行高对齐，则使用定位**

**容易出现的一个问题：**<br />[**https://www.bilibili.com/video/BV1Kg411T7t9?p=193&vd_source=7f7750324a908892d6c8486c085f335f**](https://www.bilibili.com/video/BV1Kg411T7t9?p=193&vd_source=7f7750324a908892d6c8486c085f335f)<br />**01：40~07：06**

