## hgruop包含h标签
表示文件目录

## a标签发送邮件
```html
<a href="mailto:xieranmaya@qq.com"
```

## a标签页面跳转
1. 在a标签内加上`url#｛$id｝`
2. 在目标地址的页面的目标位置元素加上`id={$id}`

## a标签的download属性
```html
<a href="url" download="xxxx.jpeg">下载图片</a>
```
这次作业因为url指向的并非图片本身，也就是地址不是url/xxxx.jpeg，所以无法直接下载，只会跳转到页面(**理解错误**)
a标签只能下载当前网页下面的文件

## pre标签
`<pre> `预定义格式文本。在该元素中的文本通常按照原文件中的编排，以等宽字体的形式展现出来，文本中的空白符（比如空格和换行符）都会显示出来。(紧跟在 <pre`>` 开始标签后的换行符也会被省略)

## input标签的hidden
1. 用于`form`标签提交提前设置好的参数
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929111440.png)
2. 可以帮`input`标签的其他属性隐藏控件

## select标签下拉选择
1. 使用option给下拉一个默认值，并且不会显示在下拉框
```html
<option selected hidden>请选择</option>
```
2. 可以使用`optgroup`给`option`分组
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929111556.png)

## 加上label和没加label有什么区别
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929111945.png)
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929112022.png)
加上label后点击"男,女"也可以选择.

## fieldset标签给表单分组/禁用input
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929111652.png)
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929134632.png)

## table标签/表格分组/列控制
1. 分组标签`thead`,`tbody`, `tfoot`, `colgroup`
2. `thead`, `tfoot`在打印超过1页内容时,会出现在每一页.如果没有则只出现在第一页.
3. 列控制 
```html
<colgroup>
	<col>      //表示第一列
	<col bgcolor="red">  //表示第二列变成红色
</colgroup>
```

## img标签usemap属性
```html
<img src="https://drscdn.500px.org/photo/174778125/m%3D1170_k%3D1/2841ccf2a3720e8e794a6a6930f6ff2c" alt="" title="image title" width="300px" usemap="#somemap">
      <map name="somemap">
        <area shape="rect" coords="63, 113, 199, 189" href="https://www.mi.com/" alt="" target="_blank">
        <area shape="circle" coords="132, 266, 50" href="" alt="">
        <area shape="poly" coords="57,82,8,265,163,397,225,256,187,83" href="" alt="">
      </map>
```
需要记住几个图形单词的简写`rect`矩形, `circle`环形, `poly`多边形

## iframe标签
在一个页面套另一个页面
```html
<iframe id="inlineFrameExample"
    title="Inline Frame Example"
    width="300"
    height="200"
    src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&layer=mapnik">
</iframe>
```
使用a标签套一个页面
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929165624.png)
iframe的浏览历史记录在嵌套的页面,可以在页面里前进后退.
