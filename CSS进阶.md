<a name="c2Z9W"></a>
# 字体图标
**对于实现简单，颜色单一的图标 可以不使用精灵图，而使用字体图标**<br />**字体图标展示的是图，但是本质是字，可以在css中通过设置文字的大小颜色**<br />**来改变字体图标的大小与颜色**

**使用：**<br />**通过link标签引入，用标签调用两个类名，一个为iconfont，一个为图标对应**<br />**的类名，来表示图标，一般采用的标签是span标签**

**需要下载后使用，下载网址是iconfont，如果网站内没有想要的字体图标，可以**<br />**在网站中上传自己的SVG矢量图转变成字体图标来使用**

<a name="J7hbj"></a>
# 平面转换
**属性名 transform： ；**<br />**改变盒子在平面上的形态（位移，缩放，旋转 旋转比较少用）**
<a name="cjdER"></a>
## 位移
**transform： translate（水平，垂直） **<br />**单位可以是px 也可以是百分比%（相对盒子自身）**<br />**水平方向右为正，垂直方向下为正**<br />**tansform: translateX（）/translateY（）；单指水平或垂直位移**

**子盒子的绝对定位居中效果里，可以用transform：translate（-50%，-50%）；**<br />**来代替**<br />**margin-left：-50%；**<br />**margin-top：-50%；**

**鼠标悬浮在.box类盒子上时，.box的after伪元素发生改变可写为**<br />**.box:hover::after{**<br />**}**
<a name="R06xa"></a>
## 旋转
**transform: rotate()；**<br />**单位为deg 代表°  正数代表顺时针 负数代表逆时针**<br />**旋转必须配合过渡属性 transition 否则没效果**

** 旋转默认是以盒子的中心作为原点围绕其旋转**<br />**可以用transform-orgin属性来改变原点（添加给盒子标签本身）**<br />**transform-orgin: 原点水平位置 ，原点垂直位置；**<br />**其值有三种取法：**<br />**1，方位名词（left，right，top，bottom，center）**<br />**2，像素px**<br />**3，百分比（相对盒子自身）**

**多重转换：**<br />**transform属性会层叠，所以如果将旋转和位移单独写，只有最后那个会生效**<br />**但是transform可以作为符合属性，但注意的是不同的属性值的顺序会导致最后的效果不同，比如 transform：translate（） rotate（）与**<br />**transform： rotate（） translate（） 产生的效果是不一样的**<br />**第一种是在位移的过程中旋转，就像汽车车轮滚动一样 **<br />**第二种是像一个漩涡一样，从漩涡中心旋转到边缘**<br />**因为第一种在位移的过程中旋转 位移的开始原点的坐标轴就已经确定 **<br />**但是第二种是旋转的过程位移，所以在位移的过程中原点的坐标轴会不断**<br />**变换，所以导致这种漩涡的效果**<br />**所以一般在复合属性中将旋转属性值放在最后 要额外注意transform属性层叠带来的影响**

<a name="bQCfH"></a>
## 缩放
**transform： scale（x轴缩放倍数，y轴缩放倍数）/（整体的缩放倍数）**<br />**此属性一般用于悬浮效果 **<br />**通过基础的css来实现悬浮时将图片放大只是将图片往**<br />**x轴y轴延伸放大，而scale是以中心为点向四周延伸放大 还是有点区别的**

**overflow:hidden; 不仅能解决浮动问题，还能将子级超出父级的那些部分隐藏；**
<a name="oTtMn"></a>
## <br />
<a name="KJFP4"></a>
## 渐变
**一般用于盒子的背景颜色渐变**<br />**background-image：linear-gradient(**<br />**颜色1,**<br />**颜色2,**<br />**颜色3,**<br />**....**<br />**）；//从颜色1过渡到颜色2过渡到颜色3**<br />**不过一般不会用颜色到颜色的过渡，那样太丑了**<br />**一般是从透明到颜色的过渡**<br />**所以属性值为**<br />**background-image：linear-gradient(**<br />**transparent(代表透明),**<br />**rgba()**<br />**）；**

<a name="zBKtm"></a>
# 空间转换
**与平面转换相识，同样使用属性transform，x，y轴与平面一致**<br />**z轴的正方向为从屏幕指向自己，相反为负方向**
<a name="yUlnU"></a>
## 位移
**相比平面位移多了一个 transform：translateZ（）；**<br />**以及transform： translate3d（x,y,z）;**

**对于z轴方向的位移，正常情况看不见，按理来说z轴正方向移动，盒子会变大**<br />**负方向移动盒子会变小，但是正常情况是没有这种效果的**<br />**得给父级元素添加透视属性 即 perspective 属性才能产生透视效果，也即视距效果（近大远小）**<br />**perspective： px； 一般取值为800~1200**<br />**其实说白了perspective是屏幕到盒子的距离**<br />**如果不添加perspective属性 默认屏幕是贴在盒子上且随盒子移动的**<br />**但是添加perspective属性后 屏幕就定在了距离那么远的一个地方 才能产生近大远小的效果**

<a name="I5SZk"></a>
## 空间旋转
**空间旋转包括围绕x，y，z，以及自定义轴旋转；**<br />**transform：rotateX（）/rotateY（）/rotateZ（）/rotateZ（x，y，z，角度）**<br />**在旋转的过程中添加透视效果能使旋转更加立体 其实平面旋转就是rotateZ旋转**<br />**即围绕盒子中心旋转**<br />**rotateZ（x，y，z，角度）几乎不使用（x，y，z取值为0~1）**

**怎么判断旋转的方向是正还是负呢：左手法则**<br />**用左手握轴，大拇指指向轴的正方向 手指弯曲的方向即为旋转的正方向 相反则为负方向**

<a name="TLB2s"></a>
## 立体呈现
<a name="ZQ1RC"></a>
### 3d效果呈现
**transform-style：perserve3d；**<br />**加在父盒子上，使子元素处于真正的3d空间中**

**比如 在父盒子fat中 两个子盒子son1 son2**<br />**让两个盒子都和父盒子一样大 则son2会被挤下去 **<br />**给son1 son2 都添加绝对定位 给父盒子添加相对定位**<br />**则只能看见son2 给fat盒子设置perserve3d属性后**<br />**让son1在y轴上移动一定距离 再让父盒子围绕y轴旋转就可以看见**<br />**立体效果son1在son2 前面**

<a name="nZQup"></a>
### 立体放大
**transform： scale3d（x，y，z）/scaleX（）/scaleY（）scaleZ（）**<br />**其实就是将盒子的长高宽放大对应倍数**

<a name="w9wJJ"></a>
# 动画
<a name="z9ZHD"></a>
## 动画的实现
**动画的实现分为两个步骤： 1，动画定义   	2，使用动画**<br />**1，定义动画**<br />**有两种定义方式**![image.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1694852646648-64434c40-c7a4-4766-ab05-491b9b07f5dd.png#averageHue=%23a0a0a0&clientId=ucaf82ef0-7942-4&from=paste&height=326&id=ub3f9ae60&originHeight=359&originWidth=1179&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=119556&status=done&style=none&taskId=ub3e0f85d-3ebc-45b1-9fc3-df2e6e40c3b&title=&width=1071.818158587149)<br />**当只有两个状态时 用第一个定义方式 如果有多个状态则用第二种**<br />**对于第一种定义方式 如果盒子的默认样式与动画的开始状态（即from的状态）一致时**<br />**可以省略from部分**<br />**对于第二种定义方式 百分比之差指的是此状态在动画时长中的占比 以图中为例**<br />**时间0%到10%的过程中都是0%里的状态 时间10%到15%的过程中都是10%里的状态**

**2，使用动画**<br />**使用动画有两种方式 都是添加在发生动画的盒子里**<br />**一种是复合属性的写法 **<br />![](https://cdn.nlark.com/yuque/0/2023/png/25687038/1694853420439-1762e2e0-c480-42fb-a0e9-6caa4835c6b1.png?x-oss-process=image%2Fresize%2Cw_825%2Climit_0#averageHue=%23e3e3e3&from=url&id=snpMY&originHeight=358&originWidth=825&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&status=done&style=none&title=)

**一种是将多个属性单独写**<br />![@E7A]R@(IX%HK4HKML~{8SQ.png](https://cdn.nlark.com/yuque/0/2023/png/25687038/1694853699499-80305170-c3e1-4e28-a602-6749618bb24d.png#averageHue=%23a3bddb&clientId=ucaf82ef0-7942-4&from=paste&height=738&id=u21f08ca9&originHeight=812&originWidth=1665&originalType=binary&ratio=1.100000023841858&rotation=0&showTitle=false&size=420115&status=done&style=none&taskId=ue0939140-984d-434b-ab96-de8b41fef5a&title=&width=1513.6363308291798)

**过渡与动画之间的关系：**<br />**如果只涉及两个状态之间的改变--使用过渡**<br />**多个状态间的变化过程以及控制变化过程--使用动画**

<a name="Vmmua"></a>
## 动画的属性值
**动画的属性值共有一下几个值**<br />**动画名称 动画时长 速度曲线 延迟时间 重复次数 动画方向 执行完毕时状态**<br />**其中动画名称以及动画时长是必须存在的，其他可选；**

<a name="u03YI"></a>
### 速度曲线
**其值有 steps(N) 代表动画分为N步，逐步进行**<br />**还有 linear  代表匀速运行，线性运行**<br />**两种值分别对应逐帧动画以及补间动画**
<a name="AU09Z"></a>
### 延迟时间
**单位为s   即秒  虽然复合属性书写没有顺序 但是因为动画时长和延迟时间单位都是s **<br />**所以当复合属性中存在两个s时 第一个为动画时长 第二个为延迟时间**
<a name="YK5yg"></a>
### 重复次数
**没有单位，数字代表重复次数  用infinite代表无限重复**
<a name="L6c56"></a>
### 动画方向
**动画默认运行是从1状态到2状态**<br />**然后重复的话就继续从1到2**<br />**当其值为alternate时 其运行状态为 从1到2 从2到1**<br />**如果有重复的话就继续循环**
<a name="axGSP"></a>
### 执行完毕时状态
**不能与重复次数和动画方向同存**<br />**只有两种值**<br />**一个是默认值backwards 即执行完毕后停留在初始态**<br />**forwards 执行完毕后停留在变化态**

<a name="LwyuH"></a>
### 暂停动画
**animation-play-state:paused；**<br />**暂停动画一般配合：hover使用**

<a name="JVsDG"></a>
## 补间动画与逐帧动画
**补间动画是一般动画采用的方式，比较平滑**<br />**逐帧动画一般只用于配合精灵图做动画**

**逐帧动画的实现： **<br />**准备显示区域---定义动画---使用动画**

**准备显示区域：盒子的尺寸与精灵图的小图一致，背景图为精灵图**<br />**定义动画：一般采用from to的形式 对于包含动画所有帧的精灵图**<br />**一般是from{**<br />**background-position：0 0；**<br />**}（一般可省 因为精灵图的默认position就是0 0）**<br />**to{**<br />**background-position：-精灵图的长 -精灵图的宽；**<br />**}**<br />**使用动画：速度曲线采用 steps（N） N与精灵图中小图的个数相同**

<a name="UBosh"></a>
## 多组动画
**格式为**<br />**animation：**<br />**动画1，**<br />**动画2，**<br />**动画3....**<br />**;**<br />**比如run动画就是两个动画的合并**<br />**一个是精灵图在盒子里的移动 产生原地踏步的效果 **<br />**一个是精灵图所在盒子的位移 产生跑步的效果**

<a name="PsHUk"></a>
# 补充
<a name="MuRhT"></a>
## **background-size: cotain/cover;**
**cotain 代表等比例放大，但当宽或高与盒子尺寸相等时，便会停止放大，所以有时不能完全覆盖住盒子；**<br />**cover 代表等比例放大，会保证完全覆盖盒子，但同时可能导致图片显示不全**

**html{**<br />**heigh：100%；**<br />**}**

**body{**<br />**heigh：100%；**<br />**}**<br />**两者代表body盒子占据整个浏览器大小**

