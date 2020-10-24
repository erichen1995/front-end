## form表单
`<form>` 元素表示文档中的一个区域，此区域包含交互控件，用于向 Web 服务器提交信息。
可以用 `:valid` 和 `:invalid` CSS 伪类来设置 `<form>` 元素的样式，此时样式的表现取决于表单中的 elements 是否有效。
关于提交表单的属性:

- `action="?c=User&a=add&id={$id}"`
- `emctype="multipart/form-data"`:当表单包含`<input type="file">`使用
- `method="post | get"`
- 



## input元素submit属性 

```html
<input type="subimt" value="提交">
```

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927173131.png)

## input元素text/password/email属性

```html
用户名: <input name="username" type="text" size="20" value="<{$user.name}>" />
密码:<input name="password" type="password" size="15" minlength="5" maxlength="15" />
邮箱:<input name="email" type="email" size="输入的最大长度" value="显示值" placeholder="提示值">
```

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927194026.png)

## input元素checkbox属性

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927193842.png)

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927193904.png)

## input元素radio多选框

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927194025.png)

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927194444.png)

## select配合option下单选择

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927194651.png)

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927194712.png)
select标签的value属性没有时选取option包裹的内容当作value

## input元素file属性

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927195202.png)

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927195220.png)
```html
<!-- 所有图片格式和文本格式 -->
<input type="file" accept="image/*, text/*">
```

## input元素button属性
```html
<!-- 用来出发js -->
<input type="button" value="按钮">
```

## input元素hidden属性

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927200953.png)

## input元素reset重置按钮

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927201009.png)

![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200927201030.png)

## textarea与label对齐问题
使用css
```html
lable {
	vertical-align: top;
}
```
