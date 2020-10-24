#html元素   #element  

## 段落元素
```html
<p>我的猫咪脾气爆:)</p>
```
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929135848.png)
## 嵌套元素
将一个元素置于其他元素中--称作嵌套
```html
<p>我的猫咪脾气<strong>爆</strong>:)</p>
```
## 空元素
不包含任何内容的元素称作--空元素
```html
<img src="images/firefox-icon.png" alt="测试图片">
```

## HTML文档详解
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>测试页面</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="测试图片">
  </body>
</html>
```
- `<!DOCTYPE html>` — 文档类型。
	- 混沌初分，HTML 尚在襁褓（大约是 1991/92 年）之时，DOCTYPE 用来链接一些 HTML 编写守则，比如自动查错之类。DOCTYPE 在当今作用有限，`仅用于保证文档正常读取`。现在知道这些就足够了。
- `<html></html> — <html>` 元素。
	- 该元素`包含整个页面的内容，也称作根元素`。
- `<head></head> — <head>` 元素。
	- 该元素的`内容对用户不可见`，其中包含例如`面向搜索引擎的搜索关键字`（keywords）、`页面描述`、`CSS 样式表`和`字符编码声明`等。
- ``<meta charset="utf-8">`` — 该元素
	- `指定文档使用 UTF-8 字符编码` ，UTF-8 包括绝大多数人类已知语言的字符。基本上 UTF-8 可以处理任何文本内容，还可以避免以后出现某些问题，没有理由再选用其他编码。
- ``<title></title>`` — \<title> 元素。
	- 该元素`设置页面的标题，显示在浏览器标签页上`，也作为收藏网页的描述文字。
- ``<body></body>`` — \<body> 元素。
	- 该元素`包含期望让用户在访问页面时看到的内容`，包括文本、图像、视频、游戏、可播放的音轨或其他内容。

## 图像
```html
<img src="images/firefox-icon.png" alt="测试图片">
```
`src`图像文件路径的地址属性.
`alt`替换文字属性,图像的描述内容.

#标记文本

## 标题
`<h1>–<h6>`用于指定内容的标题和子标题

## 段落
`<p>`用来指定段落

## 列表
1. `<ul>`无序列表（Unordered List）
2. `<ol>`有序列表（Ordered List）
- `<li>`列表项目元素
```html
<p>Mozilla 是一个全球社区，这里聚集着来自五湖四海的</p>
<ul> 
  <li>技术人员</li>
  <li>思考者</li>
  <li>建造者</li>
</ul>
<p>我们致力于……</p>
```

## 链接
`<a>`是"anchor"(锚)的缩写.
```html
<a href="https://www.baidu.com">百度</a>
```
`href`代表超文本引用(hypertext reference).

---
## HTML Base 提炼
`<p>`
`<p><strong></strong></p>`嵌套元素
`<h1>`
`<img>`空元素(不包含内容),不闭合
`<ul><li></li></ul>`无序列表
`<ol><li></li></ol>`有序列表
`<!DOCTYPE html>`仅用于保证文档正常读取,定义文本类型
`<html></html>`包含整个页面的内容,根元素
`<head></head>`	1. 面向搜索引擎的搜索关键字（keywords）、2.页面描述 3. CSS 样式表 4. 字符编码声明
`<meta charset="utf-8">`编码声明
`<title></title>`页面标题
`<body></body>`包含期望让用户在访问页面时看到的内容

---
## HTML Base 链接
`闭合标签`:两个标签把内容包含起来,就像汉堡\包子\月饼,面粉就是标签,面包\馒头\面皮就是不同的标签,馅是不同的内容.
`空标签`:相当于没有结束标签的`闭合标签`,就像没有馅的包子.
`<!DOCTYPE html>`我是html文件
`<html></html>`我里面都是html的内容
`<head></head>`	用来说明html文件内容,描述这个页面有哪些关键词,页面内容,html元素里面内容的样子,用的是哪种文字编码.
`<meta charset="utf-8">`我用的是utf8编码
`<body></body>`包含了用户看到页面时的内容