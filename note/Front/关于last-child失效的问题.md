el:last-child 匹配规则：
第一步：查找el选择器匹配元素的所有同级元素
第二步：查找同级元素中最后一个元素
第三步：检验最后一个元素是否和el匹配
```html
html：
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>

css:
.list:last-child:{border-bottom:0}
```

如果是这么写，肯定是无效的，要用一个div把这5个p包裹起来，形成闭合区间
```html
html：
<div>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
<p class="list">aaaaa</p>
</div>
css:
.list:last-child:{border-bottom:0}
```