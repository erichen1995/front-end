便签分块级和行级（内联）两种

- 块级独占一行，识别宽高
- 行级不独占，不能实质宽高，实际宽高
- 块级-> 行级 display：inline，行级->块级 display:block

W3C规范由结构、表现和行为三部分组成：

- w3c中的嵌套规范
  1. 块包行块，行包行
  2. p,h1,dt只能包含行级
  3. 块级与块级元素并列，行同
- 在开发过程中，尽量使用语义化标签。