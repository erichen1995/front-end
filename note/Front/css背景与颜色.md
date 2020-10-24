## color
设置文字的颜色会被继承，值可以是currentcolor表示当前颜色
tansparent表示透明
## linear-gradient
[[Front/mdn-css构建demo总结#css设置渐变]]

## background-image
- 值
	- url(" ")
	- linear-gradient
- 默认从`padding-box`开始渲染
- 设置为背景的图片无法直接复制

## background-size
- length
- percentage
- auto
- cover  图片填充背景，多的部分会被切掉
- contain 图片以长度大的一边显示

## object-fit
指定可替换元素的内容应该如何适应到其使用的高度和宽度确定的框
- contain 类比bg-size:contanin
- coveer  类比bg-size:cover
- fill 填充
- none 保持原有
- scale-down取none或contain中小的一个

## background-repeat
- default: repeat-xy
- repeat-x or y
- no-repeat

## background-position
- 原点：左上角
- 值： 只写一个， 另一个为center
  - length
  - percentage
  - top (length) left (length) 类比position的top...

## background-attachment
决定背景图片的位置是在窗口固定还是随着包含它的区块滚动。
- fixed 相对于窗口固定
- local 相对于元素的内容固定，元素内有滚动条，会随这滚动条滚动。
- scroll 相对元素本身固定，不会随着元素滚动条滚动而是随着元素自身的滚动而滚动



## background-origin

- 设置图片的原点位置的相对区域
- 对background-position：fixed;无效
- 值：
  - centent-box
  - padding-box
  - border-box



## background-clip

定义背景图片、颜色是否延伸到边框，内边距，内容盒子，文字。
- 需要加上`-webkit-backgroud-clip: text`
- 值
  - border-box
  - padding-box
  - content-box
  - test 如果设置为`text`，需要令`color`为`transparent`

  

## object-fit

- 同`background-size`的`contain`与`cover`效果
- 值
  - contain
  - cover



## css-sprite

将多张图标内容放在一张图上，加载时只加载一张，通过background-position定位配合图片尺寸使用。

D:\study\Front_End\Homework\miao\css-sprite.html

[[../Day/202010121433]]