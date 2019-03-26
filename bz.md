# 在此处输入标题
---**bz**的*2019.03.22*学习笔记
标签（空格分隔）： 

+ 介于之前忙于面试，知识点过得比较仓促，学得不够细致，近期学习中将会进行查漏补缺。
+ 以下来自w3school html测试问卷错题汇总
1. 在下列的 HTML 中，哪个可以添加背景颜色？
正确答案：`<body bgcolor="yellow">`
**注意！！bg！！**
2. 如何制作电子邮件链接？
正确答案：`<a href="mailto:xxx@yyy">`
**注意！！mailto！！**
3. 可以使*单元格中*的内容进行左对齐的正确 HTML 标签：
正确答案：`<td align="left">`
**valign align 的区别**
align 表示水平方向上的显示，有left/center/right
valign表示垂直上的显示，有top/middle/bottom
4. 在下列的 HTML 中，哪个可以产生下拉列表？
正确答案：`<select>`
5. 哪个可以产生文本区（textarea）？
正确答案：`<textarea>`
6. 在下列的 HTML 中，哪个可以插入背景图像？
正确答案：`<body background="background.gif">`
7. `<html lang="en">` 表示所用的语言是英文
lang在css选择器里属于**语言伪类选择器**
---**bz**的*2019.03.23*学习笔记

+ 学习资料，网站的查找与整理；
+ 学会切图；
+ 完成高数，大物作业；
+ 学会使用markdown；
+ 下载vscode插件；
+ 早睡早起为新一周熬夜做好准备（每周日是一周的第一天）。

---**bz**的*2019.03.24*学习笔记

+  **添加CSS样式**的方法:
**添加方式的优先级：按照“就近原则”：行内样式>内嵌样式>链接样式>浏览器默认样式**
1.***行内样式***：CSS样式直接添加到p标签上
`<p style="color:red;">`
2.***内嵌样式***：将CSS代码内嵌到当前页面的**head**标签部分
`<head>
   <style type="text/css">/*表示当前的样式是以CSS文本来规定的*/
     p{/*选择器开头表示作用于当前页面所有的p标签*/
       color:red;
      }
   </style>
</head>`
3.***外部式样式表文件***（后缀：.css)/*适用于多个网页文件引用*/
p{
color:red;
}

然后在**网页文件 .html**中**head**标签部分引用
/*link标签表示进行文件的链接*/
/*rel属性指要链接到什么类型的文件*/
/*href通过一个相对路径的设置，表示要链接到的文件相对位置和文件的名字*/
`<head>
 <link rel="styleheet" href="css/style.css"/>
</head>`

第三种方法的优点：

+  页面结构html代码和样式css代码的完全分离，维护方便；
+  如需改变网站风格，只需修改公共CSS文件；
+  可以在同一个html文档内部引用多个外部样式表

+  关于选择器
 +  **标签选择器**
 +  **类别选择器**（相同标签 不同样式 进行分类）
 1.css中样式的**定义**
  名字***以.开头***，后面的样式名称根据含义进行定义
 2.html中样式的**引用**
  在对应的要作用的标签之内采用它的class属性进行类别样式的引用
 + **ID选择器**/*样式被定义时具有唯一性*/
 1.css中样式的**定义**
  名字***以#开头***，后面的样式名称根据含义进行定义
 2.html中样式的**引用**
  在对应的要作用的标签之内采用它的id属性进行样式的引用

+  选择器的用法
 + 选择器的嵌套声明  空格隔开
 + 选择器的集体声明  逗号隔开
 + 选择器的全局声明  通用符选择器*
 + 选择器的混用
另有其他用法之前抄写在笔记本上，这里不加赘述

+  有关单位
单位|描述|注意
--|:--:|--
px|像素的单位 
em|字符类型的单位 1em指1个字符|自动适应用户所使用的字体 例如用户所使用的字体字号为12px 设置行高为2em 则大小为24像素
%|以百分比为单位是一个相对的概念|父层属性值的设定可由子层进行继承 默认继承父层**字体**的大小 再在此基础上设置百分比


+  有关文本
属性|描述|取值
--|:--:|--
color|颜色|
letter-spacing|字符间距|2px -3px（有相互重叠的效果）
line-height|行高|14px 1.5em（相对于文字的字号大小） 120%
text-align|对齐|left center right justify inherit
text-decoration|装饰线|none（经常设置在超链接样式的设置） overline underline line-through（删除线应用，淘宝促销商品）
text-indent|首行缩进| 2em
利用行高属性做**垂直居中**的效果
利用对齐属性做**水平居中**的效果
justify 可以使文本的两端都对齐。在两端对齐文本中，文本行的左右两端都放在**父元素的内边界**上。然后，调整单词和字母间的间隔，使各行的长度恰好相等。
问题：要由用户代理（而不是CSS）来确定两端对齐文本如何拉伸，这些做法会**影响元素的外观**，甚至改变其高度。

+  有关颜色
方法|用法|取值
--|:--:|--
颜色名|skyblue
rgb值|每个颜色分量取值0-255 rgb(x,x,x)（红，绿，蓝）|白色 rgb(255,255,255） 黑色 rgb(0,0,0)  红色 rgb（255,0,0) 三个分量**取值相等时就是灰色**
rgb百分比值|取0%-100% rgb(x%,x%,x%)
rgba|a参数值代表透明度0.0（完全透明-1.0（完全不透明）
rrggbb|十六进制数（0~9，a~f） 每两位代表一个颜色值|红色：#ff0000 去掉重复位 #f00


+  有关字体
属性|描述|取值
--|:--:|--
font|在一个声明中设置所有的字体属性|顺序：斜体 粗体 字号/行高 字体
font-family|字体系列|可以一次定义多种字体，用逗号隔开；字体名称有空格时字体以“ ”括起来，中文字体用单引号？
font-size|字号|14px 120%
font-style|斜体|italic
font-weight|粗体|bold


+  有关背景
+  元素要先添加高度和宽度，才能显示背景颜色和背景图片的效果
属性|描述|取值
--|:--:|--
background||顺序：颜色 图片 repeat
background-color||同时添加背景图片和背景颜色 **图片会覆盖颜色**
background-image|**背景图片**|需要添加一个url函数，参数双引号之内是要添加成背景图片的相对路径（相对当前网页位置图片文件所在的路径）和文件名  url（"images/logo.jpg")
background-repeat|背景图片的填充方式|


 填充|描述
--|--
repeat|作为背景图片**棋盘格**填充满整个页面，水平和垂直两个方向垂直填充
repeat-x|横向单向填充
repeat-y|纵向单项填充
no-repeat|只显示一次（很大的背景图片）


+  如何选择背景图片的填充位置?


+  有关链接（以下四个都是**伪类选择器**）
 +  顺序：LoVe&HAte
属性|描述
--|:--:
a:link|未访问
a:visited|已访问
a:hover|悬停在上方
a:active|被点击时/在文件下载过程中

超链接**动态效果**的设定
**鼠标悬停时放大字体**
a{
 font-size：：22px；
 }
a：hover{


+  有关列表（无序ol 有序ul）
属性|描述|取值
--|:--:|--
list-style|
list-style-image|为列表项标志设置图像|url（"images/logo.jpg")
list-style-position|标志的位置|inside outside
list-style-type|标志的类型


+  有关表格（大小通过width和height属性来进行设置）
table { 
width：
height：
}
属性|描述|取值
--|:--:|--
border|边框|table td th都可设置**粗细、颜色、实虚**
border-collapse|合并表格的边框和单元格的边框|border-collapse：collapse；

表格为了查看方便，隔行显示不同的颜色，需要用到**奇偶选择器**
**标签:nth-child()** 括号里可以是数字 可以是odd（表示奇数个元素）even（表示偶数个元素）
tr父元素table的第一个子元素开始，奇数个元素（**表头单元格是第一个奇数**）
第一行表头单元格利用**th**标签做出样式

+  布局和定位
+  **盒子模型**
 +  **overflow属性** 当内容溢出盒子时，overflow属性取值
属性|描述
--|--
 hidden|超出部分不可见
 scroll|显示滚动条
 auto|如果有超出部分，显示滚动条


+  
 +  border属性（还可以分方向)
属性|描述
--|--
border|顺序：width style color
border-width|px、thin、medium、thick
border-style|dashed、dotted、solid、double
border-color| 

水平分割线的制作 做一个heigh为1px的盒子


+  
 +  margin和padding属性
 对浏览器默认的设置清零
 *{
   margin：0；
   padding：0；
  }
四个方向的笔记在纸质笔记本


+  div标签做盒子的时候，有换行的效果
+  div标签做盒子的时候，**垂直方向上有一个外边距合并的效果**，合并的效果取高度高的那个作为两个盒子之间的纵向边界距离。
+  margin水平方向不会合并
+  水平居中
类型|方法
--|--
图片、文字|text-align:center;
div水平居中|margin：0 auto；
0指的是上侧和下侧的值
第二个值指的是margin-left和margin-right取值，设置为auto,浏览器会自动根据外层盒子的一个宽度和div区域的一个宽度，除以二，自动计算出margin-left和margin-right，它们是相等的，所以当前的div有水平居中的效果


+  图像框默认情况下有一个文字的默认设定空白距离？
使用font-size：0；清除


+  文档流定位，默认的html当中的元素有不同类型
+  类型的转换：display：
类型|特点|常见元素
--|--|
block|1.元素独占一行；2.元素的height、width、margin、padding可设定|`<div> <p> <h1>~<h6> <ol> <ul> <table> <form>`
inline|1.不单独占一行；2.height、width不可设；3.width是其包含的文字或图片的宽度，不可改变|`<span> <a>`
inline-block|1.不单独占一行；2.元素的height、width、margin、padding可设定|`<img>`
 **inline类型的元素水平排列开时之间有一个间距/间隙**
解决方法:将inline类型转化为block类型
用`<p>或者<ul>中的<li>`？


+  浮动定位 float clear
+  层定位 position  **不同取值决定当前定位的参照物**
定位|特征|描述
--|:--:|--
static|默认值|没有定位，top、bottom、left、right无效
fixed|固定定位|相对浏览器窗口进行定位，坐标原点始终在参照物的左上方，······有效
relative|相对定位|相对于其**直接父元素**进行定位，脱离正常的文档流中，但在文档流中的**原位置依然存在**，······有效
absolute|绝对定位|相对于**非static的第一个父元素**进行定位，脱离正常的文档流中，在文档流中的**原位置不再存在**，······有效

再解释一次：对于absolute定位的层总是相对于其最近的定义为absolute或relative的父层，而这个父层并不一定是其直接父层**。


**极端情况**
对于absolute定位的层，如果其父元素中都未定义absolute或者relative，**则其将相对body进行定位**。


**relative+absolute用法**
好处：子随父动。
父元素box1：position：relative；
子元素box2：position：absolute；（top、bottom、left、right相对于父元素来进行偏移定位。
设定子元素相对于父元素top的值是一个负数，则超出父元素的框


 +  z-index：值大在上面
 希望将图片设定为背景，将z-index设为-999；
 希望将图片设为顶层，将z-index设为999。

 +  有关可见性visibility
 值|描述
--|--
visible|默认值。元素是可见的
hidden|元素是不可见的
collapse|当在表格元素中使用时，此值可删除一行或一列，但不影响表格布局，被行或列占据的空间会留给其他元素使用。如果此值被用在其他元素上，会呈现为“hidden”。
inherit|

 
 +  图像透明度
 IE9 Firebox Chrome Opera Safari使用属性opacity来设定透明度
 **opacity属性能够设置的值从0.0到1.0.值越小，越透明。**

  IE8以及更早之前的版本使用滤镜filter：alpha（opacity=x)。x能够取的值从0到100。值越小，越透明。