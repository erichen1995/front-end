#css  #css规则集 #图像居中 
## 什么是CSS 
`CSS`:(Cascading Style Sheet)层叠样式表,是为网页添加样式的代码.

## CSS规则集详解
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929135603.png)
==**选择器（Selector）**==
HTML 元素的名称位于规则集开始。它选择了一个或多个需要添加样式的元素（在这个例子中就是 p 元素）。要给不同元素添加样式只需要更改选择器就行了。
==**声明（Declaration）**==
一个单独的规则，如 color: red; 用来指定添加样式元素的属性。
==**属性（Properties）**==
改变 HTML 元素样式的途径。（本例中 color 就是 \<p> 元素的属性。）CSS 中，由编写人员决定修改哪个属性以改变规则。
==**属性的值（Property value）**==
在属性的右边，冒号后面即属性的值，它从指定属性的众多外观中选择一个值（我们除了 red 之外还有很多属性值可以用于 color ）。
>其他重要的语法：
每个规则集（除了选择器的部分）都应该包含在成对的大括号里（{}）。
在每个声明里要用冒号（:）将属性与属性值分隔开。
在每个规则集里要用分号（;）将各个声明分隔开。
```html
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

## CSS多元素选择
选择多种类型的元素并为它们添加一组相同的样式.将不同的选择器用逗号分开.
```html
p, li, h1 {
  color: red;
}
```

## 不同类型的选择器
选择器名称 | 选择的内容 | 示例
------ |  ------ | --------|
元素选择器（也称作标签或类型选择器） | 所有指定(该)类型的 HTML 元素 | p 选择 \<p>
ID 选择器 | 具有特定 ID 的元素（单一 HTML 页面中，每个 ID 只对应一个元素，一个元素只对应一个 ID） | \#my-id 选择 \<p id="my-id"> 或 \<a id="my-id">
类选择器 | 具有特定类的元素（单一页面中，一个类可以有多个实例） | .my-class 选择 \<p class="my-class"> 和 \<a class="my-class">
属性选择器 | 拥有特定属性的元素 | img[src] 选择 \<img src="myimage.png"> 而不是 \<img>
伪（Pseudo）类选择器 | 特定状态下的特定元素（比如鼠标指针悬停） | a:hover 仅在鼠标指针悬停在链接上时选择 \<a>。

---

## 字体和文本
1. 第一步，找到之前 Google Font 输出的地址。并以 \<link> 元素的形式添加进 index.html 文档头（ \<head> 和 \</head> 之间的任意位置）。代码如下：
 \<link href="https://fonts.font.im/css?family=Open+Sans" rel="stylesheet" type="text/css"> 
以上代码为当前网页下载 Open Sans 字体，从而使自定义 CSS 中可以对 HTML 元素应用这个字体。
2. 接下来，删除 style.css 文件中已有的规则。虽然测试是成功的了，但是红字看起来并不太舒服。
3. 将下列代码添加到相应的位置，用你在 Google Fonts 找到的字体替代 font-family 中的占位行。（ font-family 意味着你想要你的文本使用的字体。）这条规则首先为整个页面设定了一个全局字体和字号（因为 \<html> 是整个页面的父元素，而且它所有的子元素都会继承相同的 font-size 和 font-family）：
```html
html {
  /* px 表示 “像素（pixels）”: 基础字号为 10 像素 */
  font-size: 10px; 
  /* Google fonts 输出的 CSS */
  font-family: 'Open Sans', sans-serif; 
}
```
4. 接下来为文档体内的元素（\<h1>、\<li> 和 \<p>）设置字号。将标题居中显示，并为正文设置行高和字间距，从而提高页面的可读性。
```html
h1 {
  font-size: 60px;
  text-align: center;
}

p, li {
  font-size: 16px;
  /* line-height 后而可以跟不同的参数，如果是数字，就是当前字体大小乘上数字 */    
  line-height: 2;
  letter-spacing: 1px;
}
```

---

## 一切皆盒子
==盒子模型==:编写 CSS 时你会发现，你的工作好像是围绕着一个一个盒子展开的——设置尺寸、颜色、位置，等等。页面里大部分 HTML 元素都可以被看作若干层叠的盒子。CSS 布局主要就是基于盒模型的。每个占据页面空间的块都有这样的属性：
- padding：即内边距，围绕着内容（比如段落）的空间。
- border：即边框，紧接着内边距的线。
- margin：即外边距，围绕元素外部的空间。
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929135624.png)

## 更改页面颜色
```html
html {
	background-color: #00539F;
}
```

## 文档体格式设置
```html
body {
  width: 600px;
  margin: 0 auto;
  background-color: #FF9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
}
```
- `width: 600px;` —— 强制页面永远保持 600 像素宽。
- `margin: 0 auto;` —— 为 margin 或 padding 等属性设置两个值时，第一个值代表元素的上方和下方（在这个例子中设置为 0），而第二个值代表左边和右边（在这里，auto 是一个特殊的值，意思是水平方向上左右对称）。你也可以使用一个，三个或四个值，参考 这里 。
- `background-color:` \#FF9500 —— 如前文所述，指定元素的背景颜色。我们给 body 用了一种略微偏红的橘色以与深蓝色的 \<html> 元素形成反差，你也可以尝试其它颜色。
- `padding: 0 20px 20px 20px;` —— 我们给内边距设置了四个值来让内容四周产生一点空间。这一次我们不设置上方的内边距，设置右边，下方，左边的内边距为20像素。值以上、右、下、左的顺序排列。
- `border: 5px solid black;` —— 直接为 body 设置 5 像素的黑色实线边框。

## 定位页面主标题并添加样式
```html
h1 {
  margin: 0;
  padding: 20px 0;    
  color: #00539F;
  text-shadow: 3px 3px 1px black;
}
```
浏览器会在没有任何 CSS 的情况下 给 \<h1> 等元素设置一些默认样式。我们通过设置 margin: 0; 来覆盖默认样式。
`text-shadow` 属性，它可以为元素中的文本提供阴影。四个值含义如下：
- 第一个值设置水平偏移值 —— 即阴影右移的像素数（负值左移）。
- 第二个值设置垂直偏移值 —— 即阴影下移的像素数（负值上移）。
- 第三个值设置阴影的模糊半径 —— 值越大产生的阴影越模糊。
- 第四个值设置阴影的基色

## 图像居中
```html
img {
  display: block;
  margin: 0 auto;
}
```
 \<body> 元素是==块级元素==，意味着它占据了页面的空间并且能够赋予外边距和其他改变间距的值。而图片是==内联元素==，不具备块级元素的一些功能。所以为了使图像有外边距，我们必须使用 `display: block` 给予其块级行为。
 
 ## CSS Base 提炼
`CSS`是为网页添加样式的代码

`css规则集`:
- ==选择器==选择一个或多个需要添加样式的元素
- ==声明==`属性`: `属性的值`;
- ==属性==改变HTML元素样式的途径.例`color`就是`\<p>`元素的属性.
- ==属性的值==例`red`是`color`的值
`CSS多元素选择`多个元素用`, `分开
`不同类型的选择器`:
- ==ID选择==如`<a id="my-id">`可以用`#my-id`选择
- ==类选择==如`<p class="my-class">`可以用`.my-class`选择
- ==属性选择==如`<a href="#" title="#"`可以用`a[href][title]`选择
- ==伪类选择==例`a.hover`用在鼠标指针悬停在链接上时选择

`字体文本`:
1. 使用`link`元素的形式添加字体进index.html文档头
2. 使用选择器选择文本,然后用`font-family`属性设定字体

`盒子模型`CSS 布局主要就是基于盒模型的,每个占据页面空间的块都有:`padding, border, margin`.
`图像居中`内联元素居中需要转为==块状元素==,`display:block`
