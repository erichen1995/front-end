## \<html lang="en">
`lang`全局属性,参与了元素语言的定义. 参与了元素语言的定义。这个语言是不可编辑元素写入的语言，或者可编辑元素应该写入的语言。标签包含单个条目，值的格式由 用于定义语言的标签 (BCP47) IETF 文档定义。如果标签的内容是空字符串，语言就设为未知。如果标签内容是无效的，根据 BCP47，它就设为无效。
????

## 在移动浏览器中使用viewport meta标签控制布局
```html
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
```
`width`属性控制视口的宽度。可以像`width=600`这样设为确切的像素数，或者设为`device-width` 特殊值，代表缩放为 100% 时以 CSS 像素计量的屏幕宽度。（相应的也有`height`及`device-height`属性，可能对包含基于视口高度调整大小及位置的元素的页面有用。）
`initial-scale` 属性控制页面最初加载时的缩放等级。`maximum-scale`、`minimum-scale`及`user-scalable`属性控制允许用户以怎样的方式放大或缩小页面。

## 媒体类型属性和值
- 有条件的通过 @media 和 @import at-rules 用CSS 装饰样式。
- 用media= 属性为\<style>,\<link>, \<source>和其他HTML元素指定特定的媒体类型。如:
```html
<link rel="stylesheet" src="styles.css" media="screen" />
<link rel="stylesheet" src="styles.css" media="print" />
```
- all 适用于所有设备
- print 用于打印预览
- screen 用于屏幕
- speech 用于语音合成器

## link标签rel="alternate"属性的作用及用法
**1. 可用于将PC版页面指向移动版页面，将移动版页面指向PC版页面，这样有利于搜索引擎，对不同设备的用户提供不同类型的页面**
PC版本页面head应添加
```html
<link rel="alternate" media="only screen and (max-width:640px)" href="http://m.mobile.com" >
```
移动版页面应添加
```html
<link rel="canonical" href="http://wwww.pc.com" >
```
**2. 用于不同css样式表之间切换控制效果**
```html
<link href="default.css" rel="stylesheet" type="text/css" title="默认">
<link href="red.css" rel="alternate stylesheet" type="text/css" title="红色">
<link href="green.css" rel="alternate stylesheet" type="text/css" title="绿色">
```
`rel=alternate`的页面是默认不会渲染的，可以作为后备样式，对link使用disabled即可进行切换，无延迟.
但是，提前下载，会浪费单宽，可以在必要的场景下使用。
??创建RSS链接
```html
<link rel="alternate" type="application/rss+xml" title="RSS" href="http://www.csszengarden.com/zengarden.xml">
```

## section element
`<section>`元素表示一个包含在HTML文档中的独立部分，它没有更具体的语义元素来表示，一般来说会有包含一个标题。
例如，导航菜单应该包含在\<nav>元素中，但搜索结果列表和地图显示及其控件没有特定元素，可以放在\<section>里。
- 一般通过是否包含一个标题 (<`h1>-<h6>` element) 作为子节点 来 辨识每一个`<section>`。
- 如果 `<section>` 元素的内容可以单独在多个媒体上发表，应该使用 `<article>` 而不是 `<section>`。
- 不要把 `<section>` 元素作为一个普通的容器来使用，这是本应该是`<div>`的用法（特别是当片段（the sectioning ）仅仅是为了美化样式的时候）。 一般来说，一个 `<section>` 应该出现在文档大纲中。



## HTML role attribute
1. 什么是role属性
   - role属性作用是告诉Accessibility类应用（比如屏幕朗读程序，为盲人提供的访问网络的便利程序）。使用role可以增强文本的可读性和语义化。
   - 在html5元素内，标签本身就是有语义的，因此role是不必添加的，至少是不推荐的，但是bootstrap的案例内很多都是有类似的属性和声明的，目的是为了兼容老版本的浏览器（用户代理），如果你的代码使用了html5标签，并且不准备支持老版本的浏览器，不妨不使用role标签。
2. 什么时候使用role
- role属性应用主要是表单,比如输入密码,对于正常人可以用**placaholder**提示输入密码，但是对于残障人士是无效的，这个时候就需要role了。另外，在老版本的浏览器中，由于不支持[HTML5](http://lib.csdn.net/base/html5)标签，所以有必要使用role属性。
3. 示例
```html
<div role="checkbox" aria-checked="checked">告诉屏幕阅读器,此处有一个复选框,且已经被选中</div>
```


## \<span> element 的用法
**`<span>`** 元素是短语内容的通用行内容器，并没有任何特殊语义。可以使用它来编组元素以达到某种样式意图（通过使用类或者Id属性），或者这些元素有着共同的属性，比如**lang**。应该在没有其他合适的语义元素时才使用它。`</span>` 与 [`<div>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div) 元素很相似，但 [`<div>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div) 是一个 [块元素](https://developer.mozilla.org/en-US/docs/HTML/Block-level_elements) 而 `<span>` 则是 [行内元素 ](https://developer.mozilla.org/en-US/docs/HTML/Inline_elements).


## \<abbr>
**缩写元素**（**`<abbr>`**）用于代表缩写，并且可以通过可选的 `title` 属性提供完整的描述。若使用 `title` 属性，则它必须且仅可包含完整的描述内容, 在鼠标指针覆盖到该元素时显示作为一个提示。。

