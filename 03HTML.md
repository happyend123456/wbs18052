# 一、HTML简介

## 1.什么是HTML？

​		HTML:Hyper Text   Markup  Language   超文本标签(标记)语言

​		由各种标签组成，用来制作网页，告诉浏览器该如何显示页面

## 2. 作用

  - 制作网页，控制网页和内容的显示
- 插入图片、音乐、视频、动画等
- 通过链接检索信息
- 使用表单获取用户信息，实现交互

## 3. 特点

​	简单、平台无关、通用

## 4. 版本

​	W3C：World   Wide  Web  Consortium  万维网联盟，制定Web技术相关的标准和规范组织，HTML就是W3C制定的标准

​	两个版本：HTML4.01 和 HTML5



## 5. 后缀名

​	HTML文件以.html或者.htm为后缀

# 二、HTML文档结构

## 1. 基本结构

 - 以html作为根标签(元素)，包含head 头部和body 主体部分
 - 头部提供关于网页的相关信息，如文档类型、字符编码、关键字等摘要信息，主体部分提供网页的具体内容，真正显示在页面中
 - 标签名不区分大小写，但一般习惯全小写

## 2. 标签组成

### 2.1 标签的组成

​	一个完整的HTML标签的组成

~~~ html
<标签名 属性名1="属性值1" 属性名2="属性值2">内容</标签名>
~~~

注意：属性值要用引号引起来，（双引号 或者 单引号）

开发工具：Sublime Text

### 2.2 标签的分类

​	根据标签是否关闭，可以分为：关闭型、非关闭型

 -  关闭型，有结束标签

    ~~~ html
    <title></title>
    <body></body>
    <h1></h1>
    ~~~

- 非关闭型，没有结束标签

  ~~~ html
  <br> 换行
  <hr> 水平线
  <meta> 
  ~~~

  根据标签是否独占一行，可以分为：块级标签、行级标签

- 块级标签，显示为块状，独自占一行

  ~~~ html
  <h1></h1>
  ~~~

- 行级标签，在行内显示，可以与其他内容在同一行显示

  ~~~ html
  <span></span>
  ~~~

  ## 3. 注释

  注释在浏览器中不会显示，但是通过查看源代码可以看到

  ~~~ html
  <!--注释内容-->
  ~~~

  注意：在注释中不要出现--

## 4. 实体字符

​	用于显示一些特殊字符，如: < 、>、&、空格等

​	语法：

~~~ html
&实体字符名称; 或者 &#实体字符编码;
~~~

常用实体字符：

~~~ html
&lt;   <
&gt;   >
&nbsp; 空格
&amp;  &
&quot; "
&copy; ©
&reg;  ®
~~~

注意：对于连续的空白字符(包含空格、缩进、换行等)，在浏览器中显示的时候都只会显示成一个空格

## 5. 文档类型

### 5.1 简介

​	使用<!DOCTYPE>声明HTML文档的类型，必须位于HTML文档的第一行

​	用来告诉浏览器页面的文档类型，通俗点说，使用的是哪个HTML版本进行编写的

​	注意：HTML4.01与HTML5之间的文档类型定义有差异

### 5.2 HTML 4.01(了解)

​	HTML4.01,<!DOCTYPE>通过引用DTD，规定了标签语言的规则，这样浏览器才能正确的显示内容

​	有三种类型的DTD：

 - STRICT严格类型，不允许弃用标记，如：font，不允许使用框架集

~~~ html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
~~~

- TRANSITIONAL过渡类型，可使用弃用标记,不允许使用框架集

~~~ html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
~~~

- FRAMESET：框架类型，可使用框架集，也是可以使用弃用标签

~~~ html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
~~~

### 5.3 HTML5

​	HTML5 不需要引用DTD，只有一种，更简单

~~~ html
<!DOCTYPE html>
~~~

# 三、HTML常用标签

### 1. 基本标签

|                |          |                           |
| -------------- | -------- | ------------------------- |
| 标签             | 含义       | 解释                        |
| br             | 换行标签     | 非关闭型                      |
| p              | 段落标签     | 独占一行，块级标签，前后有明显的间隔        |
| h1、h2、......h6 | 标题标签     | 按照h1到h6逐渐变小，独自占一行，加粗显示    |
| pre            | 预格式化文本标签 | 保留编码的格式                   |
| div            | 分区标签     | 常作为容器来使用，一般在页面布局中，块级标签    |
| span           | 范围标签     | 默认没有任何特殊的功能，一般用来设置行内的独特样式 |
| ol、li          | 有序列表     | 有顺序的项目列表                  |
| ul、li          | 无序列表     | 无顺序的项目                    |
| dl、dt、dd       | 定义列表     | 对术语、图片等进行描述定义的列表          |

### 1.1 有序列表

​	ol：ordered list

​	li：list item

​	默认使用阿拉伯的数字从1开始标记，可以通过属性进行修改

 - type属性：设置列表前的符号标记，取值：1、a小写字母、A、i罗马数字、I，默认值为1
 - start属性：设置起始值，值必须是数字

### 1.2 无序列表

​	ul：unordered list

​	li：

​	默认使用实心圆作为符号标记，可以通过属性进行修改

 - type属性：设置列表前的符号标记，取值：disc实心圆、circle空心圆、square正方形，默认取值：disc

### 1.3 定义列表

​	dl：definition  list

​	dt：definition  title

​	dd：definition  description

## 2. 常用标签

| 标签   | 含义    | 解释        |
| ---- | ----- | --------- |
| hr   | 水平线标签 | 非关闭型，块级标签 |
| img  | 图像标签  | 非关闭型，行级标签 |
|      |       |           |

### 1.1 水平线标签

​	hr：horizontal

​	常用属性：

 -  color颜色

    两种写法：

    ​	颜色名：如：red、green、blue、white、black...................

    ​	16进制的RGB：Red、Green、Blue，用法：#RRGGBB，每个颜色的范围是0-255，转换为16进制00-FF，如#FF0000、#00FF00、#FFFFFF、#000000、#CCCCCC、#AAAAAA、#FF7300（橙色）

- size 粗细

- width 宽度

  两种写法：

  ​	像素，绝对值(固定值)

  ​	百分比，相对值，相对于父容器宽度的百分比

- align 对齐

  取值：center(默认值)、left、right

###  1.2 图像标签

​	img：image

​	常见图片格式：.jpg、.png、.gif、.jpeg、.bmp......

​	常用属性：

  -   src：source 指定图片的路径，

      如果图片和html文件在同一个文件中，可以直接写图片名称

      习惯上，我们会把多个图片统一放到一个特定的文件夹中，如：images,imgs等，此时需要在图片名称前添加文件夹的名称images/

-  alt  当图片无法显示时的提示信息

-  title 当鼠标停留在图片上时候显示的提示信息

-  width/height 设置图片的宽度和高度

   默认按图片原尺寸显示

   如果只设置其中一个，则另一个按比例缩放

   如果同时设置宽和高，可能会导致图片变形

   两种写法：

   ​	像素，绝对值(固定值)

   ​	百分比，相对值，相对于父容器而言



## 3. 其他标签

| 标签      | 含义         | 解释                                   |      |      |      |
| ------- | ---------- | ------------------------------------ | ---- | ---- | ---- |
| i       | 斜体显示       | italic                               |      |      |      |
| em      | 强调的内容      | 在浏览器中显示时一般为斜体                        |      |      |      |
| address | 地址         | 在浏览器中显示时一般为斜体，独占一行，块级标签              |      |      |      |
| b       | 加粗显示       | bold                                 |      |      |      |
| strong  | 强调的内容      | 在浏览器中显示时一般为粗体                        |      |      |      |
| del     | 删除线        | delete                               |      |      |      |
| ins     | 下划线        | insert                               |      |      |      |
| small   | 相对当前字号减小一号 |                                      |      |      |      |
| big     | 相对当前字号增加一号 |                                      |      |      |      |
| sub     | 下标         |                                      |      |      |      |
| sup     | 上标         |                                      |      |      |      |
| bdo     | 设置文本方向     | 通过dir="rtl"设置文本从右到左显示（right to left） |      |      |      |
| abbr    | 设置文本缩写     |                                      |      |      |      |
|         |            |                                      |      |      |      |

## 4. 头部标签

- meta 定义网页的摘要信息，如字符编码、关键字、描述等
- title 定义网页的标题
- style 定义内部样式的css样式
- link 引用外部css样式
- script 定义或者引用脚本
- base 定义基础路径

# 四、超链接

## 1. URL

### 1.1 简介

​	URL：Uniform 	Resource 	Locator，统一资源定位符，俗称网址

​	

~~~ html
https://www.baidu.com/s?ie=utf-8&f=8&rsv_bp=1&rsv_idx=1&ch=&tn=baidu&bar=&wd=%E6%9D%A8%E5%B9%82&rn=&oq=&rsv_pq=8a1e832c000311e4&rsv_t=8b3dzeJUEtf8gwKUNNMQQlJ%2B5it8Xg0WMO1tWlHz84mf43KoifworMpyhmE&rqlang=cn
http://bbs.itany.com/portal.php
file:///D:/Users/User/Desktop/html/day02/06.%E5%85%B3%E4%BA%8E%E6%A0%87%E7%AD%BE%E7%9A%84%E5%B5%8C%E5%A5%97.html


~~~

### 1.2 组成

​	一个完整的URL由8个部分组成

- 协议 protocol 如：

  http 超文本传输协议

  ftp 文件传输协议

  file 文件协议

- 主机名：hostname ，如：ftp.itany.com、bbs.itany.com

- 端口port,位于主机名的后面，使用:分隔

  不同的协议有不同的默认端口，如：http 80 ,ftp 21

  如果使用的是默认端口，则端口可以省略

  如果使用的不是默认端口，则端口不能省略

- 路径path目标文件夹所有的路径结构

- 资源resource要访问的目标文件

- 查询字符串query string，也称为参数

  在资源后面使用?开头的一组名称/值，多个之间以&隔开，如：name=tom&age=21

- 锚点：anchor，在资源后面使用#开头的文本，如：#abc

- 身份认证 authentication指定身份信息：如：ftp://wbs18042:abc@ftp.itany.com

## 2. 超链接

### 2.1 基本用法

​	Hyper Link，使用a：anchor标签

​	语法：

~~~ html
<a href="URL" taget="链接打开位置">链接内容</a>
~~~

​	常用属性：

 -   href：链接目标

 -   target：链接打开位置，取值：

     ~~~html
     _self(当前，默认值)  、_blank(新的) 、_parent(父层框架) 、_top（顶层框架）
     ~~~

### 2.2 链接类型

​	分类：普通链接、锚链接、功能性链接

### 2.3 路径分类：

​	两种：相对路径、绝对路径

#### 2.3.1 相对路径

​	相对于当前文件的路径，如果链接目标和当前文件在同一个文件夹时可以直接写名称，如果不在同一个文件夹中，则需要使用

​	.   当前文件所在文件夹的位置

​	.. 上一级位置

#### 2.3.2 绝对路径

​	一个完整的URL

## 3. 锚链接

​	点击链接后跳转到锚点

​	使用步骤：

​	1.定义锚点

~~~ html
<a name="锚点名称"></a>
~~~

​	2.链接锚点

~~~html
<a href="#锚点名称">链接内容</a>
~~~

## 4. 功能性链接

~~~ html
<a href="javascript:alert('你是谁？嘿嘿，我是金三胖')">胖子</a>
~~~

# 五、表格

## 1. 简介

​	表格是一个规则的行列结构，每个表格由若干行组成，每行由若干单元格组成

​	table 、row 、column

## 2. 基本结构

### 2.1 table 标签

​	用来定义表格

​	常用属性：

 - border 边框，默认为0
 - width/height 宽度/高度
 - align  水平对齐，取值：left、center、right
 - bordercolor 边框颜色
 - bgcolor 背景颜色
 - background 背景图片
 - cellspacing 间距，单元格与单元格之间的距离
 - cellpadding 边距，单元格内容与边界之间的距离

### 2.2 tr 标签

​	用来定义行， table row

​	常用属性：

- align  水平对齐，取值：left、center、right
- valign 垂直对齐，取值：top、middle、bottom
- bgcolor 背景颜色
- background 背景图片



### 2.3 td 标签

​	用来定义单元格，table  data

​	常用属性：align、valign、bgcolor、background

注意：表格必须由行组成，行必须由单元格组成，数据必须放到单元格td中

### 3. 合并单元格

​	也称为表格的跨行跨列

​	两个属性：

 -  rowspan

    设置单元格所跨的行数，如rowspan="2",表示跨越2行

- colspan

  设置单元格所跨的列数，如colspan="4",表示跨越4列

步骤：

​	1.在跨越的单元格中设置rowspan/colspan属性

​	2.将被跨越的单元格删除

​	注意：必须保证每行的实际列数是相同的，否则表格可能会出现错误

## 4. 高级标签

#### 4.1 caption 标签

​	表格的标题

#### 4.2 thead 标签

​	表格的头部 table head

#### 4.3 tbody 标签

​	表格的主体 table body

​	注意：浏览器自动添加tbody

#### 4.4 tfoot 标签

​	表格的脚部  table foot

#### 4.5 th 标签

​	表格的头部的标题 table head title

​	一般用在thead中，设置头部的标题，替代td标签，与td的区别在于：加粗和居中对齐

# 六、表单

## 1. 简介

​	表单时一个包含若干表单元素的区域，用于获取不同类型的用户信息

​	表单元素是允许用户在表单中输入信息的元素，如：文本框、密码框、单选按钮、复选框、下拉列表等

## 2. 基本结构

### 2.1 表单语法

~~~ html
<form action="表单提交地址" method="提交方式">
  	多个表单元素
</form>
~~~

### 2.2 form 标签

​	用来定义表单，可以包含多个表单元素

​	常用属性：

 -  action 提交数据给谁处理，默认为当前页面

 -  method 提交数据的方式，取值：get(默认)、post

    get 和post的区别：

    ​	get：以查询字符串的形式进行提交，地址栏能看到，长度有限制，不安全

    ​	post：以表单数据组形式进行提交，地址栏中看不到，长度无限制，安全实际开发中，一般都使用post

- enctype：提交数据的编码，默认是以application/x-www-form-urlencoded，上传文件时要改为multipart/form-data



## 3. 普通表单元素

​	大多数表单元素都是使用input标签，由属性type设置表单元素的类型

~~~ html
<input type="表单元素类型">
~~~



| 表单元素类型   | 含义    | 解释                     |
| -------- | ----- | ---------------------- |
| text     | 单行文本框 | 省略不写默认就是text           |
| password | 密码框   |                        |
| radio    | 单选按钮  | 只能选择其中一个               |
| checkbox | 复选框   | 可以同时选择多个               |
| submit   | 提交按钮  | 提交表单的数据                |
| reset    | 重置按钮  | 重置表单元素的初始值             |
| image    | 图像按钮  | 可以使用图片作为按钮，也具有提交的功能    |
| button   | 普通按钮  | 默认无功能                  |
| file     | 文件选择器 | 选择要上传的文件               |
| hidden   | 隐藏域   | 在页面上不显示，但是会提交，可以用来存储数据 |

​	

#### 3.1 单行文本框

​	常用属性：

 - name名称，很重要，如果没有name，则该表单元素的数据不会被提交
 - value 初始值
 - size宽度
 - maxlength 最大字符数，默认是没有限制
 - readonly 只读，readonly="readonly“，可以简写为readonly，即只写属性名
 - disabled 禁用，disabled="disabled"，可以简写为disabled，完全不能用

注意：readonly和disabled的区别：readonly的数据可以提交，而disabled的数据不会被提交

​	表单元素被提交的两个条件：1.有name属性   2.非disabled

#### 3.2 单选按钮

​	常用属性：

 - name 名称，多个radio的name属性值必须相同，才能实现单选(互斥)
 - value值
 - checked=“checked”可以简写为checked，是否被选中，两种状态：选中、未选中

#### 3.3 复选框

​	常用属性和radio类似

#### 3.4 文件选择器

​	常用属性：

 -  name 名称

 -  accept 设置可选文件的类型，用于优先对网页上资源的类型进行区别、筛选，（当然我们也可以手动去选择所有的文件）

    常用MIME类型：

    纯文本：text/html、text/xml、text/plain

    格式文本：application/rtf、application/pdf、application/msword

    图像：image/png、image/gif、image/jpeg

    音频：audio/mpeg、audio/ogg、audio/x-wav

    视频：video/x-msvideo、video/mp4、video/quicktime



