## HTML元素属性
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929135528.png)
一个属性必须包含如下内容:
1. 一个空格,在属性和元素名称之间,属性与属性之间
2. 属性名称后面跟着一个等号
3. 属性值由一堆引号""引起来

## HTML布尔属性
`布尔属性`:没有值的属性,只能有跟它的属性名一样的属性值。
```html
<input type="text" disabled="disabled">
```
`disabled="disabled"`使得上面的表单不可用

## HTML中的空白
```html
<p>狗 狗 很 呆 萌。</p>

<p>狗 狗        很
         呆 萌。</p>
```
无论你在HTML元素的内容中使用多少空格(包括空白字符，包括换行)，当渲染这些代码的时候，HTML解释器会将连续出现的空白字符减少为一个单独的空格符。

## HTML实体引用

原义字符 | 等价字符引用
----- | ---------
< | \&lt;
> | \&gt;
" | \&quot;
' | \&apos;
& | \&amp;

## HTML注释
```html
<!-- <p>我是注释</p> -->
```
