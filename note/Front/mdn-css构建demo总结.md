## float属性无效
没有发现前面属性的分号没打，对元素样式变化不熟悉。

## em单元问题
`em`代表当前字体的大小，修改父元素的字体大小会影响子元素。
我的计算机`em`默认为16px;

## css设置外边框圆角
`border-radius`属性设置元素的外边框圆角。当使用一个半径时确定一个圆形，当使用两个半径时确定一个椭圆。这个(椭)圆与边框的交集形成圆角效果。
```css
border-radius:25%；  //四角半径都是25%
border-radius:10% / 20%;  //四角的半径分别是10%，20%

border-radius:4px 3px 6px / 2px 4px;
/*等价于*/
border-top-left-radius: 4px 2px;
border-top-right-radius: 3px 4px;
border-bottom-right-radius: 6px 2px;
border-bottom-left-radius: 3px 4px;
```

## css设置渐变
`linear-gradient()`函数创建一个两种或多种线性渐变图片。
![[Img/Pasted image 20201004184057.png]]
```css
/*0deg等于to top，180deg等于to bottom 270deg等于to left*/
background: linear-gradient(45deg, red, blue); //渐变轴从左上角45度，

/*黑色到白色渐变，白色20%才开始渐变，白色80%到黑色渐变*/
background: linear-gradient(180deg, rgba(0,0,0,0.1), white 20%, white 80%, rgba(0,0,0,0.1));

/*多个颜色的渐变*/
background: linear-gradient(to right, red, orange, yellow, green, blue, indigo, violet);
```
注意：使用`background`属性会覆盖元素原来的颜色，`background-image`则不会。

## 修改盒子模型，宽高的影响范围
```css
box-sizing: content-box;  //默认，宽高不包含padding，border，margin
box-sizing: border-box;   //宽高包含padding，border，margin
```

## 相对定位与绝对定位
绝对定位 `absolute`脱离文档流不占位置，相对定位`relative`会先放置在未添加定位时的位置，再在不改变页面布局的前提下调整元素位置（**原来的位置会空白**）。
当元素的`position`设为`absolute`时，如果父级元素没有设置`position`属性，则元素的基准点就为浏览器的**左上角**，而当父元素设置了`position`属性时，那么元素将**以父元素为基准点**。

```css
.parent {
	position: relative;
}
.child {
	position: absolute;
	bottom: 0em;   //离底部0em
	left:5 px;     //离左边5px
}

```

## 盒子阴影
`box-shadow`在元素的框架上添加阴影效果.同一个元素上设置多个阴影效果，并用逗号将他们分隔开。该属性可设置的值包括阴影的X轴偏移量、Y轴偏移量、模糊半径、扩散半径和颜色。
后写的阴影在下面
```html
  box-shadow: inset 0 -3em 3em rgba(0,0,0,0.1),  /*元素内部*/
              0 0  0 2px rgb(255,255,255),       
			  /*元素外部   x y 模糊半径 扩散半径*/
              0.3em 0.3em 1em rgba(0,0,0,0.3);
}
```